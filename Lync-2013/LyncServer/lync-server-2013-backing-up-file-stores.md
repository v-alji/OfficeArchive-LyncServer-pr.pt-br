---
title: 'Lync Server 2013: fazendo backup de armazenamentos de arquivos'
description: 'Lync Server 2013: fazendo backup de armazenamentos de arquivos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up file stores
ms:assetid: 1a7f4e93-aa3d-461e-878e-2c572baa1293
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202167(v=OCS.15)
ms:contentKeyID: 51541449
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba6a92d189c39242be1b2167ffc336d9eb406719
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438047"
---
# <a name="backing-up-file-stores-in-lync-server-2013"></a><span data-ttu-id="06946-103">Fazendo o backup de armazenamentos de arquivos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06946-103">Backing up file stores in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06946-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06946-104">

<span> </span></span></span>

<span data-ttu-id="06946-105">_**Tópico da última modificação:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="06946-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="06946-106">O backup dos repositórios de arquivos do Lync Server inclui todos os arquivos e pastas usados pelos componentes do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="06946-106">Backing up the Lync Server File Stores includes all the files and folders used by Lync Server components.</span></span>

<div>

## <a name="to-back-up-file-stores"></a><span data-ttu-id="06946-107">Para fazer backup de armazenamentos de arquivos</span><span class="sxs-lookup"><span data-stu-id="06946-107">To back up File Stores</span></span>

1.  <span data-ttu-id="06946-108">Para localizar os locais específicos dos repositórios de arquivos do Lync Server, abra o construtor de topologias e examine o nó **armazenamentos de arquivos** .</span><span class="sxs-lookup"><span data-stu-id="06946-108">To find the specific locations of your Lync Server File Stores, open Topology Builder and look in the **File stores** node.</span></span>

2.  <span data-ttu-id="06946-109">Use o Robocopy ou outra ferramenta de gerenciamento do sistema de arquivos para copiar cada repositório de arquivos para $Backup \\ filestore.</span><span class="sxs-lookup"><span data-stu-id="06946-109">Use Robocopy or another file system management tool to copy each File Store to $Backup\\filestore.</span></span>

<span data-ttu-id="06946-110"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06946-110"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

