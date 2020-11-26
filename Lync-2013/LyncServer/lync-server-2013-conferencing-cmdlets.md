---
title: 'Lync Server 2013: cmdlets de conferência'
description: 'Lync Server 2013: cmdlets de conferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferencing cmdlets
ms:assetid: 7ff94637-6319-4c45-9230-be34e8d81ede
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398641(v=OCS.15)
ms:contentKeyID: 48184640
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8b7cd9843c971d5bf8611c4e64548b2ff608f1b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434344"
---
# <a name="conferencing-cmdlets-in-lync-server-2013"></a><span data-ttu-id="14e97-103">Cmdlets de conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14e97-103">Conferencing cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="14e97-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="14e97-104">

<span> </span></span></span>

<span data-ttu-id="14e97-105">_**Tópico da última modificação:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="14e97-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="14e97-106">O Microsoft Lync Server 2013 permite que os usuários ingressem em conferências de duas maneiras diferentes: usando um aplicativo de conferência como o Lync 2013 ou discando usando um telefone.</span><span class="sxs-lookup"><span data-stu-id="14e97-106">Microsoft Lync Server 2013 enables users to join conferences in two different ways: by using a conferencing application such as Lync 2013, or by dialing in using a telephone.</span></span> <span data-ttu-id="14e97-107">Os usuários de discagem não podem fazer coisas como exibir slides ou mensagens de chat do Exchange, mas podem participar de forma completa na parte de áudio de uma conferência.</span><span class="sxs-lookup"><span data-stu-id="14e97-107">Dial-in users are not be able to do such things as view slides or exchange instant messages, but they are able to fully participate in the audio portion of a conference.</span></span>

<div>

## <a name="conferencing-cmdlets"></a><span data-ttu-id="14e97-108">Cmdlets de conferência</span><span class="sxs-lookup"><span data-stu-id="14e97-108">Conferencing Cmdlets</span></span>

<span data-ttu-id="14e97-109">Os cmdlets do **CsDialInConferencing** são usados para configurar propriedades de conferência discada, incluindo tudo, de especificar os números de telefone que os usuários podem chamar para ingressar em uma conferência para os comandos do teclado de entrada disponíveis para eles depois de ingressar em uma conferência (por exemplo, pressionar 6 para ativar ou desativar o mudo do telefone).</span><span class="sxs-lookup"><span data-stu-id="14e97-109">The **CsDialInConferencing** cmdlets are used to configure dial-in conferencing properties, including everything from specifying the phone numbers users can call in order to join a conference to the keypad commands available to them after they join a conference (for example, pressing 6 to mute or unmute their phone).</span></span> <span data-ttu-id="14e97-110">A maioria dos outros recursos de uma conferência (por exemplo, os usuários podem gravar a conferência, os usuários podem compartilhar aplicativos durante a conferência e assim por diante) são gerenciados usando cmdlets **CsConferencingPolicy** .</span><span class="sxs-lookup"><span data-stu-id="14e97-110">Most of the other features of a conference (for example, can users record the conference, can users share applications during the conference, and so on) are managed by using the **CsConferencingPolicy** cmdlets.</span></span>

<span data-ttu-id="14e97-111">**[Cmdlets de conferência discada no Lync Server 2013](lync-server-2013-dial-in-conferencing-cmdlets.md)**</span><span class="sxs-lookup"><span data-stu-id="14e97-111">**[Dial-in conferencing cmdlets in Lync Server 2013](lync-server-2013-dial-in-conferencing-cmdlets.md)**</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-112">[Get-CsConferenceDirectory](https://technet.microsoft.com/library/Gg425771(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-112">[Get-CsConferenceDirectory](https://technet.microsoft.com/library/Gg425771(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-113">[Move-CsConferenceDirectory](https://technet.microsoft.com/library/Gg412968(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-113">[Move-CsConferenceDirectory](https://technet.microsoft.com/library/Gg412968(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-114">[New-CsConferenceDirectory](https://technet.microsoft.com/library/Gg413080(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-114">[New-CsConferenceDirectory](https://technet.microsoft.com/library/Gg413080(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-115">[Remove-CsConferenceDirectory](rehttps://technet.microsoft.com/library/Gg412968(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-115">[Remove-CsConferenceDirectory](rehttps://technet.microsoft.com/library/Gg412968(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="14e97-116">[Test-CsDialInConferencing](https://technet.microsoft.com/library/Gg399013(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-116">[Test-CsDialInConferencing](https://technet.microsoft.com/library/Gg399013(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="14e97-117">[Get-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg413015(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-117">[Get-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg413015(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-118">[New-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg398818(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-118">[New-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg398818(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-119">[Remove-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg412782(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-119">[Remove-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg412782(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-120">[Set-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg425770(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-120">[Set-CsDialInConferencingAccessNumber](https://technet.microsoft.com/library/Gg425770(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="14e97-121">[Get-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg398575(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-121">[Get-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg398575(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-122">[New-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg412816(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-122">[New-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg412816(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-123">[Remove-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg398174(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-123">[Remove-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg398174(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-124">[Set-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg425825(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-124">[Set-CsDialInConferencingConfiguration](https://technet.microsoft.com/library/Gg425825(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="14e97-125">[Get-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg398578(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-125">[Get-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg398578(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-126">[New-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg425792(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-126">[New-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg425792(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-127">[Remove-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg425894(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-127">[Remove-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg425894(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-128">[Set-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg398860(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-128">[Set-CsDialInConferencingDtmfConfiguration](https://technet.microsoft.com/library/Gg398860(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="14e97-129">[Get-CsDialInConferencingLanguageList](https://technet.microsoft.com/library/Gg425869(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-129">[Get-CsDialInConferencingLanguageList](https://technet.microsoft.com/library/Gg425869(v=OCS.15))</span></span>

<span data-ttu-id="14e97-130">**[Cmdlets da webconferência no Lync Server 2013](lync-server-2013-web-conferencing-cmdlets.md)**</span><span class="sxs-lookup"><span data-stu-id="14e97-130">**[Web conferencing cmdlets in Lync Server 2013](lync-server-2013-web-conferencing-cmdlets.md)**</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-131">[Get-CsConferenceDisclaimer](https://technet.microsoft.com/library/Gg425714(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-131">[Get-CsConferenceDisclaimer](https://technet.microsoft.com/library/Gg425714(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-132">[Remove-CsConferenceDisclaimer](https://technet.microsoft.com/library/Gg398243(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-132">[Remove-CsConferenceDisclaimer](https://technet.microsoft.com/library/Gg398243(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-133">[Set-CsConferenceDisclaimer](https://technet.microsoft.com/library/Gg398776(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-133">[Set-CsConferenceDisclaimer](https://technet.microsoft.com/library/Gg398776(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="14e97-134">[Set-CsConferenceServer](https://technet.microsoft.com/library/Gg398738(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-134">[Set-CsConferenceServer](https://technet.microsoft.com/library/Gg398738(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="14e97-135">[Get-CsConferencingConfiguration](https://technet.microsoft.com/library/Gg398965(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-135">[Get-CsConferencingConfiguration](https://technet.microsoft.com/library/Gg398965(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-136">[New-CsConferencingConfiguration](https://technet.microsoft.com/library/Gg412967(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-136">[New-CsConferencingConfiguration](https://technet.microsoft.com/library/Gg412967(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-137">[Remove-CsConferencingConfiguration](https://technet.microsoft.com/library/Gg412767(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-137">[Remove-CsConferencingConfiguration](https://technet.microsoft.com/library/Gg412767(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-138">[Set-CsConferencingConfiguration](https://technet.microsoft.com/library/Gg412969(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-138">[Set-CsConferencingConfiguration](https://technet.microsoft.com/library/Gg412969(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="14e97-139">[Get-CsConferencingPolicy](https://technet.microsoft.com/library/Gg398293(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-139">[Get-CsConferencingPolicy](https://technet.microsoft.com/library/Gg398293(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-140">[Grant-CsConferencingPolicy](https://technet.microsoft.com/library/Gg425937(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-140">[Grant-CsConferencingPolicy](https://technet.microsoft.com/library/Gg425937(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-141">[New-CsConferencingPolicy](https://technet.microsoft.com/library/Gg413019(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-141">[New-CsConferencingPolicy](https://technet.microsoft.com/library/Gg413019(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-142">[Remove-CsConferencingPolicy](https://technet.microsoft.com/library/Gg398728(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-142">[Remove-CsConferencingPolicy](https://technet.microsoft.com/library/Gg398728(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-143">[Set-CsConferencingPolicy](https://technet.microsoft.com/library/Gg425788(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-143">[Set-CsConferencingPolicy](https://technet.microsoft.com/library/Gg425788(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="14e97-144">[Get-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg425875(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-144">[Get-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg425875(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-145">[New-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg398065(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-145">[New-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg398065(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-146">[Remove-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-146">[Remove-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-147">[Set-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg398648(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-147">[Set-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg398648(v=OCS.15))</span></span>

<!-- end list -->

  - <span data-ttu-id="14e97-148">[Disable-CsMeetingRoom](https://technet.microsoft.com/library/JJ204723(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-148">[Disable-CsMeetingRoom](https://technet.microsoft.com/library/JJ204723(v=OCS.15))</span></span>

  - <span data-ttu-id="14e97-149">[Enable-CsMeetingRoom](https://technet.microsoft.com/library/JJ205062(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-149">[Enable-CsMeetingRoom](https://technet.microsoft.com/library/JJ205062(v=OCS.15))</span></span>

  - <span data-ttu-id="14e97-150">[Get-CsMeetingRoom](https://technet.microsoft.com/library/JJ205277(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-150">[Get-CsMeetingRoom](https://technet.microsoft.com/library/JJ205277(v=OCS.15))</span></span>

  - <span data-ttu-id="14e97-151">[Move-CsMeetingRoom](https://technet.microsoft.com/library/JJ204889(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-151">[Move-CsMeetingRoom](https://technet.microsoft.com/library/JJ204889(v=OCS.15))</span></span>

  - <span data-ttu-id="14e97-152">[Set-CsMeetingRoom](https://technet.microsoft.com/library/JJ204831(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-152">[Set-CsMeetingRoom](https://technet.microsoft.com/library/JJ204831(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="14e97-153">[Test-CsASConference](https://technet.microsoft.com/library/JJ205227(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-153">[Test-CsASConference](https://technet.microsoft.com/library/JJ205227(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-154">[Test-CsAVConference](https://technet.microsoft.com/library/Gg412749(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-154">[Test-CsAVConference](https://technet.microsoft.com/library/Gg412749(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-155">[Test-CsDataConference](https://technet.microsoft.com/library/JJ205219(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-155">[Test-CsDataConference](https://technet.microsoft.com/library/JJ205219(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-156">[Test-CsWebApp](https://technet.microsoft.com/library/Hh689989(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-156">[Test-CsWebApp](https://technet.microsoft.com/library/Hh689989(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-157">[Test-CsWebAppAnonymous](https://technet.microsoft.com/library/Hh690041(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-157">[Test-CsWebAppAnonymous](https://technet.microsoft.com/library/Hh690041(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="14e97-158">[Test-CsWebScheduler](https://technet.microsoft.com/library/JJ204829(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="14e97-158">[Test-CsWebScheduler](https://technet.microsoft.com/library/JJ204829(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="14e97-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="14e97-159">See Also</span></span>


[<span data-ttu-id="14e97-160">Blog do PowerShell do Lync Server</span><span class="sxs-lookup"><span data-stu-id="14e97-160">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="14e97-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="14e97-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

