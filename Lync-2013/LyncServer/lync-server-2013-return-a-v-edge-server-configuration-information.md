---
title: 'Lync Server 2013: retornar informações de configuração do servidor de borda A/V'
description: 'Lync Server 2013: retorna as informações de configuração do servidor de borda A/V.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Return A/V Edge Server configuration information
ms:assetid: b041f5a4-2387-4075-846c-ec4f99640903
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721850(v=OCS.15)
ms:contentKeyID: 49733783
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4f72fccfe51b946dc0dc285aee12a07e59c844b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442471"
---
# <a name="return-av-edge-server-configuration-information-in-lync-server-2013"></a><span data-ttu-id="ce865-103">Retornar as informações de configuração do servidor de borda A/V no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce865-103">Return A/V Edge Server configuration information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce865-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce865-104">

<span> </span></span></span>

<span data-ttu-id="ce865-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="ce865-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="ce865-106">O serviço de borda A/V fornece uma maneira para seus usuários internos (usuários que estão conectados à sua rede organizacional) para compartilhar áudio e vídeo com usuários externos (usuários que não estão conectados à sua rede organizacional).</span><span class="sxs-lookup"><span data-stu-id="ce865-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="ce865-107">O serviço de borda A/V é gerenciado principalmente pelo uso de configurações de borda A/V, a configuração que pode ser configurada no escopo do site ou no escopo do serviço (ou seja, pode ser configurada para um servidor de borda A/V individual).</span><span class="sxs-lookup"><span data-stu-id="ce865-107">The A/V Edge service is primarily managed by using A/V Edge configuration settings, setting that can be configured at the site scope or at the service scope (that is, can be configured for an individual A/V Edge server).</span></span>

<span data-ttu-id="ce865-108">Para retornar informações sobre as configurações de borda a/V em uso em sua organização, você deve usar o Windows PowerShell e o cmdlet Get-CsAVEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ce865-108">To return information about the A/V Edge configuration settings in use in your organization, you must use Windows PowerShell and the Get-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="ce865-109">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [Get-CsAVEdgeConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsAVEdgeConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="ce865-109">For more information, see the help topic for the [Get-CsAVEdgeConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsAVEdgeConfiguration) cmdlet.</span></span>

<span data-ttu-id="ce865-110">As informações retornadas pelo cmdlet Get-CsAVEdgeConfiguration terão uma aparência semelhante a esta:</span><span class="sxs-lookup"><span data-stu-id="ce865-110">Information returned from the Get-CsAVEdgeConfiguration cmdlet will look similar to this:</span></span>

    Identity              : Global
    MaxTokenLifetime      : 08:00:00
    MaxBandwidthPerUserKb : 10000
    MaxBandwidthPerPortKb : 3000

<div>

## <a name="to-return-information-for-all-your-av-edge-configuration-settings"></a><span data-ttu-id="ce865-111">Para retornar informações de todas as suas configurações de borda A/V</span><span class="sxs-lookup"><span data-stu-id="ce865-111">To return information for all your A/V Edge configuration settings</span></span>

  - <span data-ttu-id="ce865-112">O comando a seguir retorna informações sobre todas as configurações de borda a/V em uso no momento em sua organização:</span><span class="sxs-lookup"><span data-stu-id="ce865-112">The following command returns information about all the A/V Edge configuration settings currently in use in your organization:</span></span>
    
        Get-CsAVEdgeConfiguration

</div>

<div>

## <a name="to-return-information-for-site-scoped-av-edge-configuration-settings"></a><span data-ttu-id="ce865-113">Para retornar informações para configurações de borda com escopo de site A/V</span><span class="sxs-lookup"><span data-stu-id="ce865-113">To return information for site-scoped A/V Edge configuration settings</span></span>

  - <span data-ttu-id="ce865-114">Para retornar informações sobre uma coleção específica de definições de configuração de borda A/V, especifique a identidade dessa coleção ao executar o cmdlet Get-CsAVEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ce865-114">To return information about a specific collection of A/V Edge configuration settings, specify the Identity of that collection when running the Get-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="ce865-115">Por exemplo, esse comando retorna informações somente para as configurações aplicadas ao site Redmond:</span><span class="sxs-lookup"><span data-stu-id="ce865-115">For example, this command returns information only for the settings applied to the Redmond site:</span></span>
    
        Get-CsAVEdgeConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-return-information-for-service-scoped-av-edge-configuration-settings"></a><span data-ttu-id="ce865-116">Para retornar informações para configurações de borda de A/V com escopo de serviço</span><span class="sxs-lookup"><span data-stu-id="ce865-116">To return information for service-scoped A/V Edge configuration settings</span></span>

  - <span data-ttu-id="ce865-117">E esse comando retorna informações somente para configurações aplicadas a um servidor de borda A/V específico:</span><span class="sxs-lookup"><span data-stu-id="ce865-117">And this command returns information only for settings applied the a specific A/V Edge server:</span></span>
    
        Get-CsAVEdgeConfiguration -Identity "service:EdgeServer:atl-edge-001.litwareinc.com"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ce865-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce865-118">See Also</span></span>


[<span data-ttu-id="ce865-119">Criar ou modificar um conjunto de configurações de servidor de borda A/V no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce865-119">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-a-v-edge-server-configuration-settings.md)  
[<span data-ttu-id="ce865-120">Excluir uma coleção existente de configurações de servidor de borda A/V no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce865-120">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-a-v-edge-server-configuration-settings.md)  


[<span data-ttu-id="ce865-121">Servidores de borda de áudio/vídeo (A/V) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce865-121">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>](lync-server-2013-audio-video-a-v-edge-servers.md)  
  

<span data-ttu-id="ce865-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce865-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

