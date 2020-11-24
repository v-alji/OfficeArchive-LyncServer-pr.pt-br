---
title: 'Lync Server 2013: importar regras de atualização de dispositivo'
description: 'Lync Server 2013: importar regras de atualização de dispositivo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Import Device Update rules
ms:assetid: 919e9c87-912b-4bc9-92e7-5998fc2e0bf0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994056(v=OCS.15)
ms:contentKeyID: 51803967
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a7b936a4b7be96332343e8f96134d5ba1b879be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390242"
---
# <a name="import-device-update-rules-in-lync-server-2013"></a><span data-ttu-id="2f4df-103">Importar regras de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f4df-103">Import Device Update rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2f4df-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2f4df-104">

<span> </span></span></span>

<span data-ttu-id="2f4df-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="2f4df-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="2f4df-106">As regras de atualização de dispositivo podem ser importadas apenas usando o Windows PowerShell e o cmdlet **Import-CsDeviceUpdate** .</span><span class="sxs-lookup"><span data-stu-id="2f4df-106">Device update rules can be imported only by using Windows PowerShell and the **Import-CsDeviceUpdate** cmdlet.</span></span> <span data-ttu-id="2f4df-107">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2f4df-107">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2f4df-108">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="2f4df-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="to-import-device-update-rules-to-a-single-web-server"></a><span data-ttu-id="2f4df-109">Para importar regras de atualização de dispositivos para um único servidor Web</span><span class="sxs-lookup"><span data-stu-id="2f4df-109">To import device update rules to a single web server</span></span>

  - <span data-ttu-id="2f4df-110">O comando a seguir importa as regras de atualização de dispositivo para o servidor Web atl-cs-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="2f4df-110">The following command imports device update rules to the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Import-CsDeviceUpdate -Identity "service:WebServer:atl-cs-001.litwareinc.com" -FileName C:\Updates\UCUpdates.cab

</div>

<div>

## <a name="to-import-device-update-rules-to-all-your-web-servers"></a><span data-ttu-id="2f4df-111">Para importar regras de atualização de dispositivos para todos os seus servidores Web</span><span class="sxs-lookup"><span data-stu-id="2f4df-111">To import device update rules to all your web servers</span></span>

  - <span data-ttu-id="2f4df-112">Neste exemplo, as regras de atualização de dispositivos são importadas para todos os servidores Web implantados em sua organização.</span><span class="sxs-lookup"><span data-stu-id="2f4df-112">In this example, device update rules are imported to all the Web servers deployed in your organization.</span></span> <span data-ttu-id="2f4df-113">Para que esse comando funcione, as atualizações de atl-fs-001.litwareinc.com de pasta \\ \\ \\ devem ser compartilhadas e disponibilizadas para todos os servidores Web.</span><span class="sxs-lookup"><span data-stu-id="2f4df-113">For this command to work, the folder \\\\atl-fs-001.litwareinc.com\\Updates must be shared and available to all the Web servers.</span></span>
    
        Get-CsService -WebServer | ForEach-Object {Import-CsDeviceUpdate -Identity $_.Identity -FileName \\atl-fs-001.litwareinc.com\Updates\UCUpdates.cab}

</div>

<span data-ttu-id="2f4df-114">Para obter detalhes, consulte o tópico da ajuda para o cmdlet [Import-CsDeviceUpdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) .</span><span class="sxs-lookup"><span data-stu-id="2f4df-114">For details, see the Help topic for the [Import-CsDeviceUpdate](https://docs.microsoft.com/powershell/module/skype/Import-CsDeviceUpdate) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2f4df-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f4df-115">See Also</span></span>


[<span data-ttu-id="2f4df-116">Exibir informações sobre as regras de atualização de dispositivos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f4df-116">View information about Device Update rules in Lync Server 2013</span></span>](lync-server-2013-view-information-about-device-update-rules.md)  
[<span data-ttu-id="2f4df-117">Aprovar uma regra de atualização de dispositivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f4df-117">Approve a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-approve-a-device-update-rule.md)  
  

<span data-ttu-id="2f4df-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2f4df-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

