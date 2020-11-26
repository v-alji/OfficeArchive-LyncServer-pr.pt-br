---
title: 'Lync Server 2013: Configurando intervalos de porta para seus clientes Microsoft Lync'
description: 'Lync Server 2013: Configurando intervalos de porta para seus clientes Microsoft Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring port ranges for your Microsoft Lync clients
ms:assetid: 287d5cea-7ada-461c-9b4a-9da2af315e71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204760(v=OCS.15)
ms:contentKeyID: 48183694
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e7fcabf81f8e0110010b1a4fb8e697fb0da986c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432727"
---
# <a name="configuring-port-ranges-for-your-microsoft-lync-clients-in-lync-server-2013"></a><span data-ttu-id="652fd-103">Configurando intervalos de porta para seus clientes do Microsoft Lync no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="652fd-103">Configuring port ranges for your Microsoft Lync clients in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="652fd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="652fd-104">

<span> </span></span></span>

<span data-ttu-id="652fd-105">_**Tópico da última modificação:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="652fd-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="652fd-106">Por padrão, os aplicativos cliente do Lync podem usar qualquer porta entre as portas 1024 e 65535 quando envolvidos em uma sessão de comunicação; Isso ocorre porque intervalos de porta específicos não são habilitados automaticamente para clientes.</span><span class="sxs-lookup"><span data-stu-id="652fd-106">By default, Lync client applications can use any port between ports 1024 and 65535 when involved in a communication session; this is because specific port ranges are not automatically enabled for clients.</span></span> <span data-ttu-id="652fd-107">No entanto, para usar a qualidade do serviço, você precisará reatribuir os vários tipos de tráfego (áudio, vídeo, mídia, compartilhamento de aplicativos e transferência de arquivos) a uma série de intervalos de porta exclusivos.</span><span class="sxs-lookup"><span data-stu-id="652fd-107">In order to use Quality of Service, however, you will need to reassign the various traffic types (audio, video, media, application sharing, and file transfer) to a series of unique port ranges.</span></span> <span data-ttu-id="652fd-108">Isso pode ser feito usando o cmdlet Set-CsConferencingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="652fd-108">This can be done by using the Set-CsConferencingConfiguration cmdlet.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="652fd-109">Os usuários finais não podem fazer essas alterações.</span><span class="sxs-lookup"><span data-stu-id="652fd-109">End users cannot make these changes themselves.</span></span> <span data-ttu-id="652fd-110">As alterações de porta só podem ser feitas por administradores usando o cmdlet Set-CsConferencingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="652fd-110">Port changes can only be made by administrators using the Set-CsConferencingConfiguration cmdlet.</span></span>



</div>

<span data-ttu-id="652fd-111">Você pode determinar quais intervalos de portas são atualmente usados para sessões de comunicação executando o seguinte comando no Shell de gerenciamento do Microsoft Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="652fd-111">You can determine which port ranges are currently used for communication sessions by running the following command from within the Microsoft Lync Server 2013 Management Shell:</span></span>

    Get-CsConferencingConfiguration

<span data-ttu-id="652fd-112">Pressupondo que você não tenha feito nenhuma alteração nas configurações de conferência desde que instalou o Lync Server 2013, você deve obter as informações que incluem esses valores de propriedade:</span><span class="sxs-lookup"><span data-stu-id="652fd-112">Assuming that you have not made any changes to your conferencing settings since you installed Lync Server 2013, you should get back information that includes these property values:</span></span>

    ClientMediaPortRangeEnabled : False
    ClientAudioPort             : 5350
    ClientAudioPortRange        : 40
    ClientVideoPort             : 5350
    ClientVideoPortRange        : 40
    ClientAppSharingPort        : 5350
    ClientAppSharingPortRange   : 40
    ClientFileTransferPort      : 5350
    ClientTransferPortRange     : 40

<span data-ttu-id="652fd-113">Se você olhar atentamente a saída anterior, verá duas coisas de importância.</span><span class="sxs-lookup"><span data-stu-id="652fd-113">If you look closely at the preceding output, you'll see two things of importance.</span></span> <span data-ttu-id="652fd-114">Primeiro, a propriedade ClientMediaPortRangeEnabled é definida como false:</span><span class="sxs-lookup"><span data-stu-id="652fd-114">First, the ClientMediaPortRangeEnabled property is set to False:</span></span>

    ClientMediaPortRangeEnabled : False

<span data-ttu-id="652fd-115">Isso é importante porque, quando essa propriedade é definida como falsa, os clientes do Lync usam qualquer porta disponível entre as portas 1024 e 65535 quando envolvidas em uma sessão de comunicação; Isso é verdadeiro independentemente de qualquer outra configuração de porta (por exemplo, ClientMediaPort ou ClientVideoPort).</span><span class="sxs-lookup"><span data-stu-id="652fd-115">That's important because, when this property is set to False, Lync clients will use any available port between ports 1024 and 65535 when involved in a communication session; this is true regardless of any other port settings (for example, ClientMediaPort or ClientVideoPort).</span></span> <span data-ttu-id="652fd-116">Se você quiser restringir o uso para um conjunto de portas especificado (e isso é algo que você deseja fazer se planejar a implementação da qualidade do serviço), primeiro você deve habilitar os intervalos de porta de mídia do cliente.</span><span class="sxs-lookup"><span data-stu-id="652fd-116">If you want to restrict usage to a specified set of ports (and this is something you do want to do if you plan on implementing Quality of Service) then you must first enable client media port ranges.</span></span> <span data-ttu-id="652fd-117">Isso pode ser feito usando o seguinte comando do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="652fd-117">That can be done using the following Windows PowerShell command:</span></span>

    Set-CsConferencingConfiguration -ClientMediaPortRangeEnabled $True

<span data-ttu-id="652fd-118">O comando anterior habilita os intervalos de porta de mídia do cliente para o conjunto global de definições de configuração de conferência; no entanto, essas configurações também podem ser aplicadas ao escopo do site e/ou ao escopo do serviço (somente para o serviço de servidor de conferência).</span><span class="sxs-lookup"><span data-stu-id="652fd-118">The preceding command enables client media port ranges for the global collection of conferencing configuration settings; however, these settings can also be applied to the site scope and/or the service scope (for the Conferencing Server service only).</span></span> <span data-ttu-id="652fd-119">Para habilitar os intervalos de porta de mídia do cliente para um site ou servidor específico, especifique a identidade desse site ou servidor ao chamar Set-CsConferencingConfiguration:</span><span class="sxs-lookup"><span data-stu-id="652fd-119">To enable client media port ranges for a specific site or server, specify the Identity of that site or server when calling Set-CsConferencingConfiguration:</span></span>

    Set-CsConferencingConfiguration -Identity "site:Redmond" -ClientMediaPortRangeEnabled $True

<span data-ttu-id="652fd-120">Ou, se preferir, você pode usar esse comando para habilitar simultaneamente intervalos de porta para todas as suas definições de configuração de conferência:</span><span class="sxs-lookup"><span data-stu-id="652fd-120">Alternatively, you can use this command to simultaneously enable port ranges for all your conferencing configuration settings:</span></span>

    Get-CsConferencingConfiguration | Set-CsConferencingConfiguration  -ClientMediaPortRangeEnabled $True

<span data-ttu-id="652fd-121">O segundo motivo da importância que você observará é que a saída do exemplo mostra que, por padrão, os intervalos de porta de mídia definidos para cada tipo de tráfego de rede são idênticos:</span><span class="sxs-lookup"><span data-stu-id="652fd-121">The second thing of importance you will notice is that the sample output shows that, by default, the media port ranges set for each type of network traffic are identical:</span></span>

    ClientAudioPort             : 5350
    ClientVideoPort             : 5350
    ClientAppSharingPort        : 5350
    ClientFileTransferPort      : 5350

<span data-ttu-id="652fd-122">Para implementar a QoS, cada um desses intervalos de portas precisará ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="652fd-122">In order to implement QoS, each of these port ranges will need to be unique.</span></span> <span data-ttu-id="652fd-123">Por exemplo, você pode configurar os intervalos de porta como este:</span><span class="sxs-lookup"><span data-stu-id="652fd-123">For example, you might configure the port ranges like this:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="652fd-124">Tipo de tráfego do cliente</span><span class="sxs-lookup"><span data-stu-id="652fd-124">Client Traffic Type</span></span></th>
<th><span data-ttu-id="652fd-125">Início da porta</span><span class="sxs-lookup"><span data-stu-id="652fd-125">Port Start</span></span></th>
<th><span data-ttu-id="652fd-126">Intervalo de porta</span><span class="sxs-lookup"><span data-stu-id="652fd-126">Port Range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="652fd-127">Áudio</span><span class="sxs-lookup"><span data-stu-id="652fd-127">Audio</span></span></p></td>
<td><p><span data-ttu-id="652fd-128">50020</span><span class="sxs-lookup"><span data-stu-id="652fd-128">50020</span></span></p></td>
<td><p><span data-ttu-id="652fd-129">cedido</span><span class="sxs-lookup"><span data-stu-id="652fd-129">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="652fd-130">Vídeo</span><span class="sxs-lookup"><span data-stu-id="652fd-130">Video</span></span></p></td>
<td><p><span data-ttu-id="652fd-131">58000</span><span class="sxs-lookup"><span data-stu-id="652fd-131">58000</span></span></p></td>
<td><p><span data-ttu-id="652fd-132">cedido</span><span class="sxs-lookup"><span data-stu-id="652fd-132">20</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="652fd-133">Compartilhamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="652fd-133">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="652fd-134">42000</span><span class="sxs-lookup"><span data-stu-id="652fd-134">42000</span></span></p></td>
<td><p><span data-ttu-id="652fd-135">cedido</span><span class="sxs-lookup"><span data-stu-id="652fd-135">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="652fd-136">Transferência de arquivos</span><span class="sxs-lookup"><span data-stu-id="652fd-136">File transfer</span></span></p></td>
<td><p><span data-ttu-id="652fd-137">42020</span><span class="sxs-lookup"><span data-stu-id="652fd-137">42020</span></span></p></td>
<td><p><span data-ttu-id="652fd-138">cedido</span><span class="sxs-lookup"><span data-stu-id="652fd-138">20</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="652fd-139">Na tabela anterior, intervalos de porta do cliente representam um subconjunto de intervalos de porta configurados para seus servidores.</span><span class="sxs-lookup"><span data-stu-id="652fd-139">In the preceding table, client port ranges represent a subset of the port ranges configured for your servers.</span></span> <span data-ttu-id="652fd-140">Por exemplo, nos servidores, o compartilhamento de aplicativos foi configurado para usar as portas 40803 a 49151; nos computadores cliente, o compartilhamento de aplicativos é configurado para usar as portas 42000 a 42019.</span><span class="sxs-lookup"><span data-stu-id="652fd-140">For example, on the servers, application sharing was configured to use ports 40803 through 49151; on the client computers, application sharing is configured to use ports 42000 through 42019.</span></span> <span data-ttu-id="652fd-141">Isso também é feito principalmente para facilitar a administração da QoS: as portas do cliente não precisam representar um subconjunto de portas usadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="652fd-141">This, too is done primarily to make administration of QoS easier: client ports do not have to represent a subset of the ports used on the server.</span></span> <span data-ttu-id="652fd-142">(Por exemplo, nos computadores cliente, você pode configurar o compartilhamento de aplicativos para usar, digamos, portas 10000 a 10019.) No entanto, é recomendável que os intervalos de porta do cliente sejam um subconjunto de intervalos de porta do servidor.</span><span class="sxs-lookup"><span data-stu-id="652fd-142">(For example, on the client computers you could configure application sharing to use, say, ports 10000 through 10019.) However, it is recommended that you make your client port ranges a subset of your server port ranges.</span></span>

<span data-ttu-id="652fd-143">Além disso, você pode ter notado que 8348 portas foram reservadas para o compartilhamento de aplicativos nos servidores, mas apenas 20 portas foram reservadas para o compartilhamento de aplicativos nos clientes.</span><span class="sxs-lookup"><span data-stu-id="652fd-143">In addition, you might have noticed that 8348 ports were set aside for application sharing on the servers, but only 20 ports were set aside for application sharing on the clients.</span></span> <span data-ttu-id="652fd-144">Isso também é recomendado, mas não é uma regra difícil e rápida.</span><span class="sxs-lookup"><span data-stu-id="652fd-144">This, too is recommended, but is not a hard-and-fast rule.</span></span> <span data-ttu-id="652fd-145">Em geral, você pode considerar cada porta disponível para representar uma única sessão de comunicação: se você tiver portas 100 disponíveis em um intervalo de porta que significa que o computador em questão pode participar, no máximo, 100 sessões de comunicação a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="652fd-145">In general, you can consider each available port to represent a single communication session: if you have 100 ports available in a port range that means that the computer in question could participate in, at most, 100 communication sessions at any given time.</span></span> <span data-ttu-id="652fd-146">Como os servidores provavelmente participarão de muitas mais conversas do que clientes, faz sentido abrir muito mais portas em servidores do que em clientes.</span><span class="sxs-lookup"><span data-stu-id="652fd-146">Because servers will likely take part in many more conversations than clients, it makes sense to open many more ports on servers than on clients.</span></span> <span data-ttu-id="652fd-147">A configuração de mais de 20 portas para compartilhamento de aplicativos em um cliente significa que um usuário pode participar de 20 sessões de compartilhamento de aplicativos no dispositivo especificado e todos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="652fd-147">Setting aside 20 ports for application sharing on a client means that a user could participate in 20 application sharing sessions on the specified device, and all at the same time.</span></span> <span data-ttu-id="652fd-148">Isso deve provar suficiente para a grande maioria dos seus usuários.</span><span class="sxs-lookup"><span data-stu-id="652fd-148">That should prove sufficient for the vast majority of your users.</span></span>

<span data-ttu-id="652fd-149">Para atribuir os intervalos de porta precedentes ao conjunto global de configurações de conferência, você pode usar o seguinte comando do Shell de gerenciamento do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="652fd-149">To assign the preceding port ranges to your global collection of conferencing configuration settings you can use the following Lync Server Management Shell command:</span></span>

    Set-CsConferencingConfiguration -Identity global -ClientAudioPort 50020 -ClientAudioPortRange 20 -ClientVideoPort 58000 -ClientVideoPortRange 20 -ClientAppSharingPort 42000 -ClientAppSharingPortRange 20 - ClientFileTransferPort 42020 -ClientFileTransferPortRange 20

<span data-ttu-id="652fd-150">Ou use este comando para atribuir esses mesmos intervalos de portas para todas as suas configurações de conferência:</span><span class="sxs-lookup"><span data-stu-id="652fd-150">Or, use this command to assign these same port ranges for all your conferencing configuration settings:</span></span>

    Get-CsConferencingConfiguration | Set-CsConferencingConfiguration -ClientAudioPort 50020 -ClientAudioPortRange 20 -ClientVideoPort 58000 -ClientVideoPortRange 20 -ClientAppSharingPort 42000 -ClientAppSharingPortRange 20 - ClientFileTransferPort 42020 -ClientFileTransferPortRange 20

<span data-ttu-id="652fd-151">Os usuários individuais devem fazer logoff do Lync e, em seguida, fazer logon novamente para que as alterações realmente entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="652fd-151">Individual users must log off from Lync and then log back on before these changes will actually take effect.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="652fd-152">Você também pode habilitar os intervalos de porta de mídia do cliente e, em seguida, atribuir esses intervalos de porta usando um único comando.</span><span class="sxs-lookup"><span data-stu-id="652fd-152">You can also enable client media port ranges, and then assign those port ranges, using a single command.</span></span> <span data-ttu-id="652fd-153">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="652fd-153">For example:</span></span><BR><CODE>Set-CsConferencingConfiguration -ClientMediaPortRangeEnabled $True -ClientAudioPort 50020 -ClientAudioPortRange 20 -ClientVideoPort 58000 -ClientVideoPortRange 20 -ClientAppSharingPort 42000 -ClientAppSharingPortRange 20 -ClientFileTransferPort 42020 -ClientFileTransferPortRange 20</CODE>



<span data-ttu-id="652fd-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="652fd-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

