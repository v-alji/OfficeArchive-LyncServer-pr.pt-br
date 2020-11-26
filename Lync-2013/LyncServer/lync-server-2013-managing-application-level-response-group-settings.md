---
title: 'Lync Server 2013: gerenciar configurações de grupo de resposta no nível do aplicativo'
description: 'Lync Server 2013: Gerenciando configurações de grupo de resposta em nível de aplicativo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing application-level Response Group settings
ms:assetid: aab749a1-fa2d-4ce8-a6c6-ebcfa37ce02a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721843(v=OCS.15)
ms:contentKeyID: 49733776
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd362cbe8ce738a16639b89edd79439b564444ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425994"
---
# <a name="managing-application-level-response-group-settings-in-lync-server-2013"></a><span data-ttu-id="d3fc9-103">Gerenciando configurações de grupo de resposta no nível do aplicativo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3fc9-103">Managing application-level Response Group settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3fc9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3fc9-104">

<span> </span></span></span>

<span data-ttu-id="d3fc9-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="d3fc9-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="d3fc9-106">As configurações no nível do aplicativo para o aplicativo de grupo de resposta incluem a configuração de música em espera padrão, o arquivo de áudio de música em espera padrão, o período de cortesia do agente e a configuração do contexto de chamada.</span><span class="sxs-lookup"><span data-stu-id="d3fc9-106">Application-level settings for Response Group application include the default music-on-hold configuration, the default music-on-hold audio file, the agent ringback grace period, and the call context configuration.</span></span> <span data-ttu-id="d3fc9-107">Você pode definir apenas um conjunto de configurações do aplicativo por pool.</span><span class="sxs-lookup"><span data-stu-id="d3fc9-107">You can define only one set of application-level settings per pool.</span></span> <span data-ttu-id="d3fc9-108">Para exibir as configurações do aplicativo, use o cmdlet **Get-CsRgsConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="d3fc9-108">To view application-level settings, use the **Get-CsRgsConfiguration** cmdlet.</span></span> <span data-ttu-id="d3fc9-109">Para modificar as configurações do aplicativo, use o cmdlet **Set-CsRgsConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="d3fc9-109">To modify the application-level settings, use the **Set-CsRgsConfiguration** cmdlet.</span></span>

<span data-ttu-id="d3fc9-p102">A música de espera padrão é tocada quando uma chamada é coloca em espera, apenas se nenhuma música de espera personalizada for definida. O contexto de chamada está disponível somente para filas atribuídas aos fluxos de trabalho interativos. Se o contexto de chamada for ativado, um agente poderá ver informações como o tempo de espera do chamador ou perguntas e respostas do fluxo de trabalho quando a chamada for recebida.</span><span class="sxs-lookup"><span data-stu-id="d3fc9-p102">The default music on hold is played when a call is placed on hold only if no custom music on hold is defined. Call context is available only for queues assigned to interactive workflows. If call context is enabled, an agent can see information such as caller wait time or workflow questions and answers when the call is received.</span></span>

<div>

## <a name="to-modify-response-group-application-level-settings"></a><span data-ttu-id="d3fc9-113">Para modificar as configurações em nível de aplicativo de grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="d3fc9-113">To modify Response Group application-level settings</span></span>

1.  <span data-ttu-id="d3fc9-114">Faça logon como um membro do grupo RTCUniversalServerAdmins ou como um membro de uma das funções administrativas predefinidas que oferecem suporte ao Grupo de Resposta.</span><span class="sxs-lookup"><span data-stu-id="d3fc9-114">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="d3fc9-115">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="d3fc9-115">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="d3fc9-116">Na linha de comando, execute:</span><span class="sxs-lookup"><span data-stu-id="d3fc9-116">At the command line, run:</span></span>
    
        Set-CsRgsConfiguration -Identity <name of service hosting Response Group> [-AgentRingbackGracePeriod <# seconds until call returns to agent after declined>] [-DefaultMusicOnHoldFile <audio file>] [-DisableCallContext <$true | $false>]
    
    <span data-ttu-id="d3fc9-117">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d3fc9-117">For example:</span></span>
    
        Set-CsRgsConfiguration -Identity "service:ApplicationServer:redmond.contoso.com" -AgentRingbackGracePeriod 30 -DisableCallContext $false
    
    <span data-ttu-id="d3fc9-p103">Para especificar um arquivo de áudio para ser usado como a música de espera padrão, você precisa primeiro importar o arquivo de áudio. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d3fc9-p103">To specify an audio file to use as the default music on hold, you need to import the audio file first. For example:</span></span>
    
        $x = Import-CsRgsAudioFile -Identity "service:ApplicationServer:redmond.contoso.com" -FileName "MusicWhileYouWait.wav" -Content (Get-Content C:\Media\ MusicWhileYouWait.wav -Encoding byte -ReadCount 0)
        Set-CsRgsConfiguration -Identity "service:ApplicationServer:redmond.contoso.com" -DefaultMusicOnHoldFile <$x>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d3fc9-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3fc9-120">See Also</span></span>


[<span data-ttu-id="d3fc9-121">Get-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3fc9-121">Get-CsRgsConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration)  
[<span data-ttu-id="d3fc9-122">Set-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3fc9-122">Set-CsRgsConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsRgsConfiguration)  
[<span data-ttu-id="d3fc9-123">Import-CsRgsAudioFile</span><span class="sxs-lookup"><span data-stu-id="d3fc9-123">Import-CsRgsAudioFile</span></span>](https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile)  
  

<span data-ttu-id="d3fc9-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3fc9-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

