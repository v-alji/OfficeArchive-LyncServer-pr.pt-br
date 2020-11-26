---
title: Mover objetos de contato da Unificação de mensagens do Exchange
description: Mover objetos de contato da Unificação de mensagens do Exchange.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move Exchange Unified Messaging Contact objects
ms:assetid: 35c7e987-41b5-4798-b617-3303f20e52e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688022(v=OCS.15)
ms:contentKeyID: 49733612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e3353427f407523a8778585d27201355714a3085
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438439"
---
# <a name="move-exchange-unified-messaging-contact-objects"></a><span data-ttu-id="16814-103">Mover objetos de contato da Unificação de mensagens do Exchange</span><span class="sxs-lookup"><span data-stu-id="16814-103">Move Exchange Unified Messaging Contact objects</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16814-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16814-104">

<span> </span></span></span>

<span data-ttu-id="16814-105">_**Tópico da última modificação:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="16814-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="16814-106">Para migrar os objetos de contato do atendedor automático (AA) e do nome do assinante (SA) para a nova implantação do Lync Server 2013, primeiro mova os objetos da implantação herdada do Office Communications Server 2007 R2 para a nova implantação do Lync Server 2013 usando os cmdlets **Get-CsExUmContact** e **move-CsExUmContact** .</span><span class="sxs-lookup"><span data-stu-id="16814-106">To migrate Auto Attendant (AA) and Subscriber Access (SA) contact objects to the new Lync Server 2013 deployment, you first move the objects from the legacy Office Communications Server 2007 R2 deployment to the new the Lync Server 2013 deployment using the **Get-CsExUmContact** and **Move-CsExUmContact** cmdlets.</span></span> <span data-ttu-id="16814-107">No servidor Exchange, você executa o script **ExchUCUtil** do Windows PowerShell para fazer o seguinte para o pool do Lync recém implantado:</span><span class="sxs-lookup"><span data-stu-id="16814-107">On the Exchange Server, you then run the **ExchUCUtil** Windows PowerShell script to do the following for the newly deployed Lync pool:</span></span>

  - <span data-ttu-id="16814-108">Adicione-o aos gateways IP de Unificação de mensagens.</span><span class="sxs-lookup"><span data-stu-id="16814-108">Add it to the Unified Messaging IP gateways.</span></span>

  - <span data-ttu-id="16814-109">Adicione-o aos grupos coletivos de Unificação de mensagens.</span><span class="sxs-lookup"><span data-stu-id="16814-109">Add it to the Unified Messaging hunt groups.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="16814-110">Para usar os cmdlets <STRONG>Get-CsExUmContact</STRONG> e <STRONG>move-CsExUmContact</STRONG> , você deve ser membro do grupo RTCUniversalUserAdmins e ter permissão de unidade organizacional (OU) para a UO em que os objetos de contatos estão armazenados.</span><span class="sxs-lookup"><span data-stu-id="16814-110">In order to use the <STRONG>Get-CsExUmContact</STRONG> and <STRONG>Move-CsExUmContact</STRONG> cmdlets, you must be a member of the RTCUniversalUserAdmins group and have organizational unit (OU) permission to the OU where the contacts objects are stored.</span></span> <span data-ttu-id="16814-111">É possível conceder permissão de OU ao usar o cmdlet <STRONG>Grant-OUPermission</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="16814-111">OU permission can be granted using the <STRONG>Grant-OUPermission</STRONG> cmdlet.</span></span>



</div>

<div>

## <a name="to-move-contact-objects-by-using-the-lync-server-management-shell"></a><span data-ttu-id="16814-112">Para mover objetos de contato usando o Shell de gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="16814-112">To move contact objects by using the Lync Server Management Shell</span></span>

1.  <span data-ttu-id="16814-113">Abra o Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="16814-113">Open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="16814-114">Para cada pool registrado no Exchange UM (onde pool1.contoso.net é um pool da implantação do Office Communications Server 2007 R2 e pool2.contoso.net é o pool da implantação do Lync Server 2013) na linha de comando, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="16814-114">For each pool registered with Exchange UM (where pool1.contoso.net is a pool from the Office Communications Server 2007 R2 deployment and pool2.contoso.net is the pool from the Lync Server 2013 deployment) at the command line, type the following:</span></span>
    
        Get-CsExUmContact -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsExUmContact -Target pool02.contoso.net
    
    <span data-ttu-id="16814-115">Para verificar se os objetos de contato foram movidos, execute o cmdlet **Get-CsExumContact** e confirme se **RegistrarPool** agora está apontando para o novo pool.</span><span class="sxs-lookup"><span data-stu-id="16814-115">To verify that the contact objects are moved, run the **Get-CsExumContact** cmdlet and confirm that **RegistrarPool** is now pointing to the new pool.</span></span>

</div>

<div>

## <a name="to-run-the-exchucutil-windows-powershell-script"></a><span data-ttu-id="16814-116">Para executar o script do Windows PowerShell ExchUCUtil</span><span class="sxs-lookup"><span data-stu-id="16814-116">To run the ExchUCUtil Windows PowerShell script</span></span>

1.  <span data-ttu-id="16814-117">Faça logon no servidor Exchange UM como usuário com privilégios de administrador da organização do Exchange.</span><span class="sxs-lookup"><span data-stu-id="16814-117">Log on to the Exchange UM Server as a user with Exchange Organization Administrator privileges.</span></span>

2.  <span data-ttu-id="16814-118">Navegue até o script ExchUCUtil do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="16814-118">Navigate to the ExchUCUtil Windows PowerShell script.</span></span>
    
    <span data-ttu-id="16814-119">No Exchange 2007, ExchUCUtil.ps1 está localizado em: **% arquivos de programas \\ % \\ scripts do Microsoft Exchange Server \\ \\ExchUCUtil.ps1**</span><span class="sxs-lookup"><span data-stu-id="16814-119">In Exchange 2007, ExchUCUtil.ps1 is located at: **%Program Files%\\Microsoft\\Exchange Server\\Scripts\\ExchUCUtil.ps1**</span></span>
    
    <span data-ttu-id="16814-120">No Exchange 2010, ExchUCUtil.ps1 está localizado em: **% arquivos de programas% \\ Microsoft \\ Exchange Server \\ v14 \\ scripts \\ExchUCUtil.ps1**</span><span class="sxs-lookup"><span data-stu-id="16814-120">In Exchange 2010, ExchUCUtil.ps1 is located at: **%Program Files%\\Microsoft\\Exchange Server\\V14\\Scripts\\ExchUCUtil.ps1**</span></span>

3.  <span data-ttu-id="16814-121">Se o Exchange estiver implantado em uma única floresta, digite:</span><span class="sxs-lookup"><span data-stu-id="16814-121">If Exchange is deployed in a single forest, type:</span></span>
    
        exchucutil.ps1
    
    <span data-ttu-id="16814-122">Ou, se o Exchange estiver implantado em várias florestas, digite:</span><span class="sxs-lookup"><span data-stu-id="16814-122">Or, if Exchange is deployed in multiple forests, type:</span></span>
    
        exchucutil.ps1 -Forest:" <forest FQDN>"
    
    <span data-ttu-id="16814-123">em que floresta FQDN especifica a floresta na qual o Lync Server 2013 é implantado.</span><span class="sxs-lookup"><span data-stu-id="16814-123">where forest FQDN specifies the forest in which Lync Server 2013 is deployed.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="16814-124">Não se esqueça de reiniciar o serviço de <STRONG>front-end do Lync Server</STRONG> (rtcsrv.exe) <EM>após</EM> a execução do exchucutil.ps1.</span><span class="sxs-lookup"><span data-stu-id="16814-124">Be sure to restart the <STRONG>Lync Server Front-End</STRONG> service (rtcsrv.exe) <EM>after</EM> you run exchucutil.ps1.</span></span> <span data-ttu-id="16814-125">Caso contrário, o Lync Server 2013 não irá detectar a Unificação de mensagens na topologia.</span><span class="sxs-lookup"><span data-stu-id="16814-125">Otherwise, Lync Server 2013 will not detect Unified Messaging in the topology.</span></span>

    
    <span data-ttu-id="16814-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16814-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

