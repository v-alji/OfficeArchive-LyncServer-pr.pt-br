---
title: 'Lync Server 2013: Configurando intervalos de porta para seus servidores de conferência, aplicativo e mediação'
description: 'Lync Server 2013: Configurando intervalos de porta para seus servidores de conferência, aplicativo e mediação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring port ranges for your Conferencing, Application, and Mediation servers
ms:assetid: 4d6eaa5d-0127-453f-be6a-e55384772d83
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204872(v=OCS.15)
ms:contentKeyID: 48184074
ms.date: 05/01/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eb3f51e42c86b667b6990f41640bf09e12e840c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432755"
---
# <a name="configuring-port-ranges-in-lync-server-2013-for-your-conferencing-application-and-mediation-servers"></a><span data-ttu-id="2627e-103">Configurando intervalos de porta no Lync Server 2013 para servidores de conferência, aplicativo e mediação</span><span class="sxs-lookup"><span data-stu-id="2627e-103">Configuring port ranges in Lync Server 2013 for your Conferencing, Application, and Mediation servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2627e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2627e-104">

<span> </span></span></span>

<span data-ttu-id="2627e-105">_**Tópico da última modificação:** 2015-04-30_</span><span class="sxs-lookup"><span data-stu-id="2627e-105">_**Topic Last Modified:** 2015-04-30_</span></span>

<span data-ttu-id="2627e-106">Para implementar a qualidade do serviço, você deve configurar intervalos de porta idênticos para compartilhamento de áudio, vídeo e aplicativos em seus servidores de conferência, aplicativo e mediação; Além disso, esses intervalos de portas não devem ser sobrepostos de maneira alguma.</span><span class="sxs-lookup"><span data-stu-id="2627e-106">In order to implement Quality of Service, you should configure identical port ranges for audio, video, and application sharing on your Conferencing, Application, and Mediation servers; furthermore, those port ranges must not overlap in any way.</span></span> <span data-ttu-id="2627e-107">Para usar um exemplo simples, suponha que você use as portas 10000 a 10999 para vídeo em seus servidores de conferência.</span><span class="sxs-lookup"><span data-stu-id="2627e-107">To use a simple example, suppose you use ports 10000 through 10999 for video on your Conferencing servers.</span></span> <span data-ttu-id="2627e-108">Isso significa que você também deve reservar as portas de 10000 a 10999 para o vídeo em seus servidores de aplicativo e mediação.</span><span class="sxs-lookup"><span data-stu-id="2627e-108">That means that you must also reserve ports 10000 through 10999 for video on your Application and Mediation servers.</span></span> <span data-ttu-id="2627e-109">Se você não fizer isso, a QoS não funcionará conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="2627e-109">If you do not, QoS will not work as expected.</span></span>

<span data-ttu-id="2627e-110">Da mesma forma, suponha que você reserve portas de 10000 a 10999 para vídeo, mas Reserve portas de 10500 a 11999 para áudio.</span><span class="sxs-lookup"><span data-stu-id="2627e-110">Similarly, suppose you reserve ports 10000 through 10999 for video, but then reserve ports 10500 through 11999 for audio.</span></span> <span data-ttu-id="2627e-111">Isso pode criar problemas para a qualidade do serviço, pois os intervalos de porta se sobrepõem.</span><span class="sxs-lookup"><span data-stu-id="2627e-111">This can create problems for Quality of Service, because the port ranges overlap.</span></span> <span data-ttu-id="2627e-112">Com a QoS, cada modalidade deve ter um conjunto exclusivo de portas: se você usar as portas 10000 a 10999 para vídeo, será necessário usar um intervalo diferente (por exemplo, 11000 a 11999 para áudio).</span><span class="sxs-lookup"><span data-stu-id="2627e-112">With QoS, each modality must have a unique set of ports: if you use ports 10000 through 10999 for video, then you'll have to use a different range (for example, 11000 through 11999 for audio).</span></span>

<span data-ttu-id="2627e-113">Por padrão, os intervalos de porta de áudio e vídeo não se sobrepõem no Microsoft Lync Server 2013; no entanto, os intervalos de porta atribuídos ao compartilhamento de aplicativos se sobrepõem com os intervalos de porta de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="2627e-113">By default, audio and video port ranges do not overlap in Microsoft Lync Server 2013; however, the port ranges assigned to application sharing overlap with both the audio and video port ranges.</span></span> <span data-ttu-id="2627e-114">(Que, por sua vez, significa que nenhum desses intervalos é exclusivo.) Você pode verificar os intervalos de porta existentes para seus servidores de conferência, aplicativo e mediação executando os três comandos a seguir no Shell de gerenciamento do Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="2627e-114">(Which, in turn, means that none of these ranges are unique.) You can verify the existing port ranges for your Conferencing, Application, and Mediation servers by running the following three commands from within the Lync Server 2013 Management Shell:</span></span>

    Get-CsService -ConferencingServer | Select-Object Identity, AudioPortStart, AudioPortCount, VideoPortStart, VideoPortCount, AppSharingPortStart, AppSharingPortCount
    
    Get-CsService -ApplicationServer | Select-Object Identity, AudioPortStart, AudioPortCount
    
    Get-CsService -MediationServer | Select-Object Identity, AudioPortStart, AudioPortCount

<div>


> [!WARNING]  
> <span data-ttu-id="2627e-115">Como você pode ver nos comandos anteriores, cada tipo de porta – áudio, vídeo e compartilhamento de aplicativos – recebe dois valores de propriedade separados: o início da porta e a contagem de portabilidade.</span><span class="sxs-lookup"><span data-stu-id="2627e-115">As you can see in the preceding commands, each port type – audio, video, and application sharing – is assigned two separate property values: the port start and the port count.</span></span> <span data-ttu-id="2627e-116">A porta Start indica a primeira porta usada para essa modalidade; por exemplo, se o início da porta de áudio for igual a 50000, isso significa que a primeira porta usada para tráfego de áudio é a porta 50000.</span><span class="sxs-lookup"><span data-stu-id="2627e-116">The port start indicates the first port used for that modality; for example, if the audio port start is equal to 50000 that means that the first port used for audio traffic is port 50000.</span></span> <span data-ttu-id="2627e-117">Se o número da porta de áudio for 2 (que não é um valor válido, mas é usado aqui para fins de ilustração), isso significa que apenas duas portas são alocadas para áudio.</span><span class="sxs-lookup"><span data-stu-id="2627e-117">If the audio port count is 2 (which is not a valid value, but is used here for illustration purposes) that means that only 2 ports are allocated for audio.</span></span> <span data-ttu-id="2627e-118">Se a primeira porta for a porta 50000 e houver um total de duas portas, isso significa que a segunda porta deve ser a porta 50001 (intervalos de porta devem ser contíguos).</span><span class="sxs-lookup"><span data-stu-id="2627e-118">If the first port is port 50000 and there are a total of two ports, that means the second port must be port 50001 (port ranges have to be contiguous).</span></span> <span data-ttu-id="2627e-119">Como resultado, o intervalo de porta para áudio seria a porta 50000 a 50001, inclusive.</span><span class="sxs-lookup"><span data-stu-id="2627e-119">As a result, the port range for audio would be ports 50000 through 50001, inclusive.</span></span><BR><span data-ttu-id="2627e-120">Observe que o servidor de aplicativos e o servidor de mediação também dão suporte a QoS para áudio; Você não precisa alterar as portas de vídeo ou de compartilhamento de aplicativos em seus servidores de aplicativos ou servidores de mediação.</span><span class="sxs-lookup"><span data-stu-id="2627e-120">Note, too that Application server and Mediation server only support QoS for audio; you do not need to change video or application sharing ports in your Application servers or Mediation servers.</span></span>



</div>

<span data-ttu-id="2627e-121">Se você executar os três comandos anteriores, verá que os valores de porta padrão para o Lync Server 2013 são configurados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2627e-121">If you run the preceding three commands you'll see that the default port values for Lync Server 2013 are configured like this:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2627e-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2627e-122">Property</span></span></th>
<th><span data-ttu-id="2627e-123">Servidor de conferência</span><span class="sxs-lookup"><span data-stu-id="2627e-123">Conferencing Server</span></span></th>
<th><span data-ttu-id="2627e-124">Servidor de aplicativos</span><span class="sxs-lookup"><span data-stu-id="2627e-124">Application Server</span></span></th>
<th><span data-ttu-id="2627e-125">Servidor de Mediação</span><span class="sxs-lookup"><span data-stu-id="2627e-125">Mediation Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2627e-126">AudioPortStart</span><span class="sxs-lookup"><span data-stu-id="2627e-126">AudioPortStart</span></span></p></td>
<td><p><span data-ttu-id="2627e-127">49152</span><span class="sxs-lookup"><span data-stu-id="2627e-127">49152</span></span></p></td>
<td><p><span data-ttu-id="2627e-128">49152</span><span class="sxs-lookup"><span data-stu-id="2627e-128">49152</span></span></p></td>
<td><p><span data-ttu-id="2627e-129">49152</span><span class="sxs-lookup"><span data-stu-id="2627e-129">49152</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2627e-130">AudioPortCount</span><span class="sxs-lookup"><span data-stu-id="2627e-130">AudioPortCount</span></span></p></td>
<td><p><span data-ttu-id="2627e-131">8348</span><span class="sxs-lookup"><span data-stu-id="2627e-131">8348</span></span></p></td>
<td><p><span data-ttu-id="2627e-132">8348</span><span class="sxs-lookup"><span data-stu-id="2627e-132">8348</span></span></p></td>
<td><p><span data-ttu-id="2627e-133">8348</span><span class="sxs-lookup"><span data-stu-id="2627e-133">8348</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2627e-134">VideoPortStart</span><span class="sxs-lookup"><span data-stu-id="2627e-134">VideoPortStart</span></span></p></td>
<td><p><span data-ttu-id="2627e-135">57501</span><span class="sxs-lookup"><span data-stu-id="2627e-135">57501</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2627e-136">VideoPortCount</span><span class="sxs-lookup"><span data-stu-id="2627e-136">VideoPortCount</span></span></p></td>
<td><p><span data-ttu-id="2627e-137">8034</span><span class="sxs-lookup"><span data-stu-id="2627e-137">8034</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2627e-138">ApplicationSharingPortStart</span><span class="sxs-lookup"><span data-stu-id="2627e-138">ApplicationSharingPortStart</span></span></p></td>
<td><p><span data-ttu-id="2627e-139">49152</span><span class="sxs-lookup"><span data-stu-id="2627e-139">49152</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2627e-140">ApplicationSharingPortCount</span><span class="sxs-lookup"><span data-stu-id="2627e-140">ApplicationSharingPortCount</span></span></p></td>
<td><p><span data-ttu-id="2627e-141">16383</span><span class="sxs-lookup"><span data-stu-id="2627e-141">16383</span></span></p></td>
<td><p>--</p></td>
<td><p>--</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2627e-142">Conforme observado anteriormente, ao configurar as portas do Lync Server para QoS, certifique-se de que: 1) as configurações da porta de áudio sejam idênticas nos seus servidores de conferência, aplicativo e mediação; e, 2) os intervalos de porta não se sobrepõem.</span><span class="sxs-lookup"><span data-stu-id="2627e-142">As noted previously, when configuring Lync Server ports for QoS, you should ensure that: 1) audio port settings are identical across yours Conferencing, Application, and Mediation servers; and, 2) port ranges do not overlap.</span></span> <span data-ttu-id="2627e-143">Se você olhar atentamente para a tabela anterior, verá que os intervalos de porta são idênticos nos três tipos de servidor.</span><span class="sxs-lookup"><span data-stu-id="2627e-143">If you look closely at the preceding table, you will see that the port ranges are identical across the three server types.</span></span> <span data-ttu-id="2627e-144">Por exemplo, a porta de áudio inicial é definida como a porta 49152 em cada tipo de servidor e o número total de portas reservadas para áudio em cada servidor também é idêntica: 8348.</span><span class="sxs-lookup"><span data-stu-id="2627e-144">For example, the starting audio port is set to port 49152 on each server type, and the total number of ports reserved for audio in each server is also identical: 8348.</span></span> <span data-ttu-id="2627e-145">No entanto, os intervalos de porta sobrepõem: as portas de áudio começam na porta 49152, mas as portas se reservam para o compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2627e-145">However, the port ranges overlap: audio ports start at port 49152, but so do the ports set aside for application sharing.</span></span> <span data-ttu-id="2627e-146">Para fazer uso ideal da qualidade do serviço, o compartilhamento de aplicativos deve ser reconfigurado para usar um intervalo de porta exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2627e-146">In order to make optimal use of Quality of Service, application sharing should be reconfigured to use a unique port range.</span></span> <span data-ttu-id="2627e-147">Por exemplo, você pode configurar o compartilhamento de aplicativos para iniciar na porta 40803 e para usar as portas do 8348.</span><span class="sxs-lookup"><span data-stu-id="2627e-147">For example, you could configure application sharing to start at port 40803 and to use 8348 ports.</span></span> <span data-ttu-id="2627e-148">(Por que 8348 portas?</span><span class="sxs-lookup"><span data-stu-id="2627e-148">(Why 8348 ports?</span></span> <span data-ttu-id="2627e-149">Se você adicionar esses valores juntos--40803 + 8348-------------------------49150 40803--</span><span class="sxs-lookup"><span data-stu-id="2627e-149">If you add those values together -- 40803 + 8348 -- that means that application sharing will use ports 40803 through port 49150.</span></span> <span data-ttu-id="2627e-150">Como as portas de áudio não começam até a porta 49152, você não terá mais nenhum intervalo de portas sobrepostos.)</span><span class="sxs-lookup"><span data-stu-id="2627e-150">Because audio ports do not begin until port 49152, you will no longer have any overlapping port ranges.)</span></span>

<span data-ttu-id="2627e-151">Depois de selecionar o novo intervalo de porta para compartilhamento de aplicativos, você pode fazer a alteração usando o cmdlet Set-CsConferencingServer.</span><span class="sxs-lookup"><span data-stu-id="2627e-151">After you have selected the new port range for application sharing you can make your change by using the Set-CsConferencingServer cmdlet.</span></span> <span data-ttu-id="2627e-152">Essa alteração não precisa ser feita em seus servidores de aplicativos ou em seus servidores de mediação, pois esses servidores não manipulam o tráfego de compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2627e-152">This change does not need to be made on your Application servers or on your Mediation servers, because these servers do not handle application sharing traffic.</span></span> <span data-ttu-id="2627e-153">Você só precisa alterar valores de porta nestes servidores se decidir reatribuir as portas usadas para tráfego de áudio.</span><span class="sxs-lookup"><span data-stu-id="2627e-153">You only need to change port values on these servers if you decide to reassign the ports used for audio traffic.</span></span>

<span data-ttu-id="2627e-154">Para modificar os valores de porta para compartilhamento de aplicativos em um único servidor de conferência, execute um comando semelhante a isso dentro do Shell de gerenciamento do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="2627e-154">To modify the port values for application sharing on a single Conferencing server run a command similar to this from within the Lync Server Management Shell:</span></span>

    Set-CsConferenceServer -Identity ConferencingServer:atl-cs-001.litwareinc.com -AppSharingPortStart 40803 -AppSharingPortCount 8348

<span data-ttu-id="2627e-155">Se você quiser fazer essas alterações em todos os seus servidores de conferência, poderá executar esse comando em vez disso:</span><span class="sxs-lookup"><span data-stu-id="2627e-155">If you want to make these changes on all your Conferencing servers you can run this command instead:</span></span>

    Get-CsService -ConferencingServer | ForEach-Object {Set-CsConferenceServer -Identity $_.Identity -AppSharingPortStart 40803 -AppSharingPortCount 8348}

<span data-ttu-id="2627e-156">Depois de alterar as configurações de porta, você deve parar e reiniciar cada serviço afetado pelas alterações.</span><span class="sxs-lookup"><span data-stu-id="2627e-156">After changing port settings you should stop and then restart each service affected by the changes.</span></span>

<span data-ttu-id="2627e-157">Não é obrigatório que seus servidores de conferência, servidores de aplicativos e servidores de mediação compartilhem exatamente o mesmo intervalo de porta; o único requisito verdadeiro é que você se reservasse intervalos de porta exclusivos em todos os seus servidores.</span><span class="sxs-lookup"><span data-stu-id="2627e-157">It is not mandatory that your Conferencing servers, Application servers, and Mediation servers share the exact same port range; the only true requirement is that you set aside unique port ranges on all your servers.</span></span> <span data-ttu-id="2627e-158">No entanto, a administração normalmente será mais fácil se você usar o mesmo conjunto de portas em todos os seus servidores.</span><span class="sxs-lookup"><span data-stu-id="2627e-158">However, administration will typically be easier if you use the same set of ports on all your servers.</span></span>

<span data-ttu-id="2627e-159"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2627e-159"></div>

<span> </span>

</div>

</div>

</span></span></div>

