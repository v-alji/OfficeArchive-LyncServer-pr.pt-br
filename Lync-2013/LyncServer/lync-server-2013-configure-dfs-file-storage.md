---
title: 'Lync Server 2013: Configurar armazenamento de arquivo'
description: 'Lync Server 2013: configurar o armazenamento de arquivos DFS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DFS file storage
ms:assetid: a985be20-5a00-4f38-b45b-83dc82de3827
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205150(v=OCS.15)
ms:contentKeyID: 48185037
ms.date: 05/23/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d70ae93db188ec51d04dd33d6c3cb5659db5a2c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390367"
---
# <a name="configure-dfs-file-storage-for-lync-server-2013"></a><span data-ttu-id="49cdd-103">Configurar armazenamento de arquivo para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="49cdd-103">Configure DFS file storage for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="49cdd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="49cdd-104">

<span> </span></span></span>

<span data-ttu-id="49cdd-105">_**Tópico da última modificação:** 2016-05-23_</span><span class="sxs-lookup"><span data-stu-id="49cdd-105">_**Topic Last Modified:** 2016-05-23_</span></span>

<span data-ttu-id="49cdd-106">O Lync Server 2013 oferece suporte ao uso de compartilhamentos de arquivos em um sistema de arquivos distribuídos (DFS).</span><span class="sxs-lookup"><span data-stu-id="49cdd-106">Lync Server 2013 supports using file shares on a Distributed File System (DFS).</span></span> <span data-ttu-id="49cdd-107">Para obter detalhes sobre o DFS para Windows Server 2008, consulte o guia passo a passo do DFS para Windows Server 2008 em [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835) . Para usar um DFS, o Lync Server 2013 requer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="49cdd-107">For details about DFS for Windows Server 2008, see the DFS Step-by-Step Guide for Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835).To use a DFS, Lync Server 2013 requires the following:</span></span>

  - <span data-ttu-id="49cdd-108">Namespaces são baseados em domínio</span><span class="sxs-lookup"><span data-stu-id="49cdd-108">Namespaces are domain based</span></span>

  - <span data-ttu-id="49cdd-109">Todos os servidores de namespace estão executando no mínimo um Windows 2008</span><span class="sxs-lookup"><span data-stu-id="49cdd-109">All namespace servers are running a minimum of Windows 2008</span></span>

<span data-ttu-id="49cdd-110">O programa de instalação do Lync Server 2013 exige que as permissões em uma pasta compartilhada permitam acesso total ao administrador.</span><span class="sxs-lookup"><span data-stu-id="49cdd-110">Lync Server 2013 setup requires that permissions on shared folder allow full access to Administrator.</span></span> <span data-ttu-id="49cdd-111">O Lync Server 2013 usará as permissões de arquivo NTFS para ACL nas pastas.</span><span class="sxs-lookup"><span data-stu-id="49cdd-111">Lync Server 2013 will then use NTFS file permissions to ACL the folders.</span></span> <span data-ttu-id="49cdd-112">As permissões de compartilhamento DFS herdadas não serão usadas para restringir o acesso.</span><span class="sxs-lookup"><span data-stu-id="49cdd-112">Inherited DFS share permissions will not be used to restrict access.</span></span>

<span data-ttu-id="49cdd-113">Para obter mais detalhes sobre os requisitos de compartilhamento de arquivos, consulte [suporte de armazenamento de arquivos no Lync Server 2013](lync-server-2013-file-storage-support.md) na documentação de suporte.</span><span class="sxs-lookup"><span data-stu-id="49cdd-113">For more details about File Share requirements, see [File storage support in Lync Server 2013](lync-server-2013-file-storage-support.md) in the Supportability documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="49cdd-114">Você pode estar procurando por informações sobre como configurar um compartilhamento não DFS.</span><span class="sxs-lookup"><span data-stu-id="49cdd-114">You may be looking for information on configuring a non-DFS share.</span></span> <span data-ttu-id="49cdd-115">Em caso afirmativo, confira <A href="lync-server-2013-hardware-setup.md">a configuração de hardware do Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="49cdd-115">If so, check out <A href="lync-server-2013-hardware-setup.md">Hardware setup for Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="49cdd-116">O procedimento a seguir descreve como configurar corretamente as permissões de pasta compartilhada usando o assistente de namespace do DFS (conforme descrito no guia de configuração do DFS).</span><span class="sxs-lookup"><span data-stu-id="49cdd-116">The following procedure describes how to correctly configure shared folder permissions using the DFS Namespace Wizard (as described in DFS setup guide).</span></span>

<div>

## <a name="to-configure-shared-folder-permissions"></a><span data-ttu-id="49cdd-117">Para configurar permissões de pasta compartilhada</span><span class="sxs-lookup"><span data-stu-id="49cdd-117">To configure shared folder permissions</span></span>

1.  <span data-ttu-id="49cdd-118">Clique em **Iniciar**, aponte para **todos os programas**, aponte para **Ferramentas administrativas** e clique em **Gerenciamento DFS**.</span><span class="sxs-lookup"><span data-stu-id="49cdd-118">Click **Start**, point to **All Programs**, point to **Administrative Tools**, and then click **DFS Management**.</span></span>

2.  <span data-ttu-id="49cdd-119">Na árvore de console do snap-in Gerenciamento DFS, clique com o botão direito do mouse no servidor de namespace (por exemplo, filesrv1.contoso.com) e, em seguida, clique em **Editar configurações**.</span><span class="sxs-lookup"><span data-stu-id="49cdd-119">In the console tree of the DFS Management snap-in, right-click the namespace server (for example filesrv1.contoso.com), and then click **Edit Settings**.</span></span>

3.  <span data-ttu-id="49cdd-120">Selecione **permissões de pasta compartilhada**.</span><span class="sxs-lookup"><span data-stu-id="49cdd-120">Select **Shared Folder Permissions**.</span></span>

4.  <span data-ttu-id="49cdd-121">Selecione **usar permissões personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="49cdd-121">Select **Use Custom Permissions**.</span></span>

5.  <span data-ttu-id="49cdd-122">Para o grupo administrador, selecione o seguinte em **permitir**:</span><span class="sxs-lookup"><span data-stu-id="49cdd-122">For the Administrator group, select the following under **Allow**:</span></span>
    
      - <span data-ttu-id="49cdd-123">**Controle total**</span><span class="sxs-lookup"><span data-stu-id="49cdd-123">**Full Control**</span></span>
    
      - <span data-ttu-id="49cdd-124">**Alteração**</span><span class="sxs-lookup"><span data-stu-id="49cdd-124">**Change**</span></span>
    
      - <span data-ttu-id="49cdd-125">**Ler**</span><span class="sxs-lookup"><span data-stu-id="49cdd-125">**Read**</span></span>

6.  <span data-ttu-id="49cdd-126">Clique em **aplicar** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="49cdd-126">Click **Apply**, and then click **OK**.</span></span>

<span data-ttu-id="49cdd-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="49cdd-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

