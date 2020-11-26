---
title: 'Lync Server 2013: restaurando um armazenamento de arquivos'
description: 'Lync Server 2013: restaurando um armazenamento de arquivos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring a file store
ms:assetid: 89916fc6-31d3-4c7f-9eaf-c02584761ef4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202180(v=OCS.15)
ms:contentKeyID: 51541491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 201c4b20f224fa3a25e931689e564410c60143e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436248"
---
# <a name="restoring-a-file-store-in-lync-server-2013"></a><span data-ttu-id="a111e-103">Restaurando um armazenamento de arquivos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a111e-103">Restoring a file store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a111e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a111e-104">

<span> </span></span></span>

<span data-ttu-id="a111e-105">_**Tópico da última modificação:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="a111e-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="a111e-106">Os repositórios de arquivos para a edição Standard estão geralmente localizados no servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="a111e-106">File Stores for Standard Edition are typically located on the Standard Edition server.</span></span> <span data-ttu-id="a111e-107">O armazenamento de arquivos para Enterprise Edition geralmente está localizado em um servidor de arquivos ou cluster.</span><span class="sxs-lookup"><span data-stu-id="a111e-107">File Stores for Enterprise Edition are typically located on a file server or cluster.</span></span> <span data-ttu-id="a111e-108">O procedimento a seguir descreve como restaurar um armazenamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a111e-108">The following procedure describes how to restore a File Store.</span></span>

<div>

## <a name="to-restore-a-file-store"></a><span data-ttu-id="a111e-109">Para restaurar um armazenamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="a111e-109">To restore a File Store</span></span>

1.  <span data-ttu-id="a111e-110">Se um armazenamento de arquivos falhar, copie o armazenamento de arquivos apropriado de $Backup \\ para o local do repositório de arquivos no servidor de arquivos ou no servidor Standard Edition e, em seguida, compartilhe a pasta.</span><span class="sxs-lookup"><span data-stu-id="a111e-110">If a File Store fails, copy the appropriate File Store from $Backup\\ to the File Store location on the file server or Standard Edition server, and then share the folder.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="a111e-111">O caminho e o nome do arquivo do repositório de arquivos restaurados devem ser exatamente os mesmos do armazenamento de arquivos de backup, para que os componentes que usam os arquivos possam acessá-los.</span><span class="sxs-lookup"><span data-stu-id="a111e-111">The path and file name for the restored File Store should be exactly the same as the backed up File Store, so that components that use the files can access them.</span></span>

    
    </div>

2.  <span data-ttu-id="a111e-112">Se necessário, defina as listas de controle de acesso (ACLs) para o repositório de arquivos.</span><span class="sxs-lookup"><span data-stu-id="a111e-112">If necessary, set the access control lists (ACLs) for the File Store.</span></span> <span data-ttu-id="a111e-113">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="a111e-113">At the command line, type:</span></span>
    
        Enable-CsTopology
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a111e-114">Você só precisará executar essa etapa se não tiver executado o construtor de topologias durante o processo de restauração.</span><span class="sxs-lookup"><span data-stu-id="a111e-114">You need to perform this step only if you have not otherwise run Topology Builder during your restoration process.</span></span>

    
    <span data-ttu-id="a111e-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a111e-115"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

