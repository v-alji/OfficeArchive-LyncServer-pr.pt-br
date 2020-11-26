---
title: 'Lync Server 2013: Suporte a armazenamento de arquivo'
description: Suporte ao armazenamento de arquivos do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: File storage support
ms:assetid: ed66430d-3c19-4267-938c-956a51005073
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399073(v=OCS.15)
ms:contentKeyID: 48185743
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03b7c3379c6aad6283f6a55b991ebaec50044bda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428173"
---
# <a name="file-storage-support-in-lync-server-2013"></a><span data-ttu-id="65ba7-103">Suporte a armazenamento de arquivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65ba7-103">File storage support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="65ba7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="65ba7-104">

<span> </span></span></span>

<span data-ttu-id="65ba7-105">_**Tópico da última modificação:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="65ba7-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="65ba7-106">O Lync Server 2013 usa o mesmo armazenamento de arquivos para todo o armazenamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="65ba7-106">Lync Server 2013 uses the same file store for all file storage.</span></span> <span data-ttu-id="65ba7-107">O suporte para armazenamento de arquivos inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="65ba7-107">File storage support includes the following:</span></span>

  - <span data-ttu-id="65ba7-108">Um compartilhamento de arquivos no armazenamento de conexão direta (DAS) ou em uma rede de área de armazenamento (SAN), incluindo o sistema de arquivos distribuídos (DFS) e uma matriz redundante de discos independentes (RAID) para armazenamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="65ba7-108">A file share on either direct attached storage (DAS) or a storage area network (SAN), including Distributed File System (DFS), and on a redundant array of independent disks (RAID) for file stores.</span></span> <span data-ttu-id="65ba7-109">Para obter detalhes sobre requisitos de armazenamento, consulte [requisitos técnicos para servidores front-end, mensagens instantâneas e presença no Lync server 2013](lync-server-2013-technical-requirements-for-front-end-servers-instant-messaging-and-presence.md) e [requisitos de hardware e software para o diretor do Lync Server 2013](lync-server-2013-hardware-and-software-requirements-for-the-director.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="65ba7-109">For details about storage requirements, see [Technical requirements for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-technical-requirements-for-front-end-servers-instant-messaging-and-presence.md) and [Hardware and software requirements for the Director in Lync Server 2013](lync-server-2013-hardware-and-software-requirements-for-the-director.md) in the Planning documentation.</span></span> <span data-ttu-id="65ba7-110">Para obter detalhes sobre o sistema operacional do DFS para Windows Server 2008, consulte o guia passo a passo do DFS para Windows Server 2008 em [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835) .</span><span class="sxs-lookup"><span data-stu-id="65ba7-110">For details about DFS for Windows Server 2008 operating system, see the DFS Step-by-Step Guide for Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835).</span></span>

  - <span data-ttu-id="65ba7-111">Um cluster compartilhado para o compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="65ba7-111">A shared cluster for the file share.</span></span> <span data-ttu-id="65ba7-112">Se você usa um cluster compartilhado, deve usar os servidores de cluster que executam o Windows Server 2008 ou o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="65ba7-112">If you use a shared cluster, you should use cluster servers running Windows Server 2008 or Windows Server 2008 R2.</span></span> <span data-ttu-id="65ba7-113">Usar servidores de cluster executando uma versão mais antiga do Windows pode resultar em problemas de permissão que impedem a disponibilidade de alguns recursos.</span><span class="sxs-lookup"><span data-stu-id="65ba7-113">Using cluster servers running an older version of Windows may result in permission issues that prevent some features from being available.</span></span> <span data-ttu-id="65ba7-114">Use o administrador de cluster para criar os compartilhamentos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="65ba7-114">Use the Cluster Administrator to create the file shares.</span></span> <span data-ttu-id="65ba7-115">Para obter detalhes sobre como usar o administrador de cluster, consulte o artigo 284838 da base de dados de conhecimento Microsoft, "como criar um compartilhamento de arquivos de cluster de servidor com o Cluster.exe" em [https://go.microsoft.com/fwlink/p/?linkId=140899](https://go.microsoft.com/fwlink/p/?linkid=140899) .</span><span class="sxs-lookup"><span data-stu-id="65ba7-115">For details about using the Cluster Administrator, see Microsoft Knowledge Base article 284838, "How to Create a Server Cluster File Share with Cluster.exe" at [https://go.microsoft.com/fwlink/p/?linkId=140899](https://go.microsoft.com/fwlink/p/?linkid=140899).</span></span>

<span data-ttu-id="65ba7-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="65ba7-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

