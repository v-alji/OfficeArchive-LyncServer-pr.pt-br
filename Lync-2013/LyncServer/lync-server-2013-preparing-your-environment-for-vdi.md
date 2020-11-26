---
title: 'Lync Server 2013: Preparando seu ambiente para VDI'
description: 'Lync Server 2013: preparando seu ambiente para VDI.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing your environment for VDI
ms:assetid: a3ec2e13-1a73-4b1c-a54a-8db7d4cd50f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205154(v=OCS.15)
ms:contentKeyID: 48185052
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e90b9e0f09d3082a28406f1a1dc715285ee4d7e3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424083"
---
# <a name="preparing-your-lync-server-2013-environment-for-vdi"></a><span data-ttu-id="d59be-103">Preparando seu ambiente no Lync Server 2013 para VDI</span><span class="sxs-lookup"><span data-stu-id="d59be-103">Preparing your Lync Server 2013 environment for VDI</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d59be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d59be-104">

<span> </span></span></span>

<span data-ttu-id="d59be-105">_**Tópico da última modificação:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="d59be-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="d59be-106">Para preparar o ambiente para o plug-in VDI do Lync, o administrador deve executar as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="d59be-106">To prepare the environment for the Lync VDI plug-in, the administrator must perform the following steps.</span></span>

1.  <span data-ttu-id="d59be-107">No Lync Server 2013, certifique-se de que EnableMediaRedirection está definido como TRUE para todos os usuários do VDI.</span><span class="sxs-lookup"><span data-stu-id="d59be-107">In Lync Server 2013, ensure that EnableMediaRedirection is set to TRUE for all VDI users.</span></span> <span data-ttu-id="d59be-108">Para obter detalhes, consulte os tópicos da ajuda para o cmdlet [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) e o cmdlet [set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) .</span><span class="sxs-lookup"><span data-stu-id="d59be-108">For details, see the Help topics for the [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) cmdlet and the [Set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) cmdlet.</span></span>

2.  <span data-ttu-id="d59be-109">No computador do Data Center, instale o cliente do Lync 2013 em todas as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="d59be-109">On the data center computer, install the Lync 2013 client on all virtual machines.</span></span>

3.  <span data-ttu-id="d59be-110">Nos computadores locais, instale o plug-in VDI do Lync.</span><span class="sxs-lookup"><span data-stu-id="d59be-110">On the local computers, install the Lync VDI plug-in.</span></span>

<span data-ttu-id="d59be-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d59be-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

