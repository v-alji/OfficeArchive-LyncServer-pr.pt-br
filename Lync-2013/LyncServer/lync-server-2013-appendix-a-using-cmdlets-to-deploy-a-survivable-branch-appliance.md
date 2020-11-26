---
title: 'Lync Server 2013: Anexo A: Usando cmdlets para implantar uma Aparelho de Filial Persistente'
description: 'Lync Server 2013: Apêndice A: usar cmdlets para implantar um aparelho de ramificação sobreviventes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Appendix A: Using cmdlets to deploy a Survivable Branch Appliance'
ms:assetid: 796a26cf-7ec9-453b-8757-6153a6dd86c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398598(v=OCS.15)
ms:contentKeyID: 48184569
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6bf1fe5d86900ec5da95ed9020720149a5015f19
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440644"
---
# <a name="appendix-a-using-cmdlets-to-deploy-a-survivable-branch-appliance-in-lync-server-2013"></a><span data-ttu-id="5b652-103">Anexo A: Usando cmdlets para implantar uma Aparelho de Filial Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b652-103">Appendix A: Using cmdlets to deploy a Survivable Branch Appliance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b652-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b652-104">

<span> </span></span></span>

<span data-ttu-id="5b652-105">_**Tópico da última modificação:** 2012-10-07_</span><span class="sxs-lookup"><span data-stu-id="5b652-105">_**Topic Last Modified:** 2012-10-07_</span></span>

<span data-ttu-id="5b652-106">Este tópico descreve como implantar um aparelho de ramificação sobreviventes usando o Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5b652-106">This topic describes how to deploy a Survivable Branch Appliance using the Lync Server Management Shell.</span></span> <span data-ttu-id="5b652-107">Execute este procedimento no site central.</span><span class="sxs-lookup"><span data-stu-id="5b652-107">Perform this procedure at the central site.</span></span>

<div>

## <a name="to-deploy-a-survivable-branch-appliance-remotely"></a><span data-ttu-id="5b652-108">Para implantar um aparelho de ramificação sobreviventes remotamente</span><span class="sxs-lookup"><span data-stu-id="5b652-108">To deploy a Survivable Branch Appliance remotely</span></span>

1.  <span data-ttu-id="5b652-109">Siga o procedimento em [adicionar sites de filiais à sua topologia no Lync Server 2013](lync-server-2013-add-branch-sites-to-your-topology.md) para adicionar um novo site de filial.</span><span class="sxs-lookup"><span data-stu-id="5b652-109">Follow the procedure in [Add branch sites to your topology in Lync Server 2013](lync-server-2013-add-branch-sites-to-your-topology.md) to add a new branch site.</span></span>

2.  <span data-ttu-id="5b652-110">Ingresse no site de filial para o domínio.</span><span class="sxs-lookup"><span data-stu-id="5b652-110">Join the branch site to the domain.</span></span>

3.  <span data-ttu-id="5b652-111">Adicione o grupo RTCUniversalSBATechnicians ao grupo Administradores local.</span><span class="sxs-lookup"><span data-stu-id="5b652-111">Add the RTCUniversalSBATechnicians group to the local Administrators group.</span></span>

4.  <span data-ttu-id="5b652-112">Reinicie o servidor e faça logon como membro do grupo RTCUniversalSBATechnicians.</span><span class="sxs-lookup"><span data-stu-id="5b652-112">Restart the server, and log on to it as a member of the RTCUniversalSBATechnicians group.</span></span>

5.  <span data-ttu-id="5b652-113">No Shell de gerenciamento do Lync Server, digite os seguintes comandos, substituindo os espaços reservados pelas informações corretas para a sua organização:</span><span class="sxs-lookup"><span data-stu-id="5b652-113">In the Lync Server Management Shell, type the following commands, replacing the placeholders with the correct information for your organization:</span></span>
    
        Export-CsConfiguration -FileName C:\CSConfig.zip
        Import-CsConfiguration -LocalStore -FileName C:\CSConfig.zip -Verbose
        Enable-CSReplica -Verbose
        Enable-CsComputer -Verbose
        Request-CsCertificate -New -Type default -CA <YourCA> -Verbose
        Set-CsCertificate -Type Default -Thumbprint <YourCertThumbprint>
        Start-cswindowsservice -verbose

<span data-ttu-id="5b652-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b652-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

