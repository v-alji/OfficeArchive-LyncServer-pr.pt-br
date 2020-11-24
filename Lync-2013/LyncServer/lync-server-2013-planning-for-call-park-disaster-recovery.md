---
title: 'Lync Server 2013: Planejamento para recuperação de desastre de Estacionamento de Chamada'
description: 'Lync Server 2013: planejando a recuperação de desastres do parque da chamada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Call Park disaster recovery
ms:assetid: f7cf3958-177b-4340-a864-35a6f44d6d88
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205395(v=OCS.15)
ms:contentKeyID: 48185867
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1d05503f1d8c30f4dd4446a995442d5e2500dbc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389687"
---
# <a name="planning-for-call-park-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="a3e44-103">Planejamento para recuperação de desastre de Estacionamento de Chamada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3e44-103">Planning for Call Park disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3e44-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3e44-104">

<span> </span></span></span>

<span data-ttu-id="a3e44-105">_**Tópico da última modificação:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="a3e44-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="a3e44-106">Esta seção descreve algumas maneiras de preparar o aplicativo parque de chamadas para a recuperação de desastres e algumas considerações para o processo de recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="a3e44-106">This section describes some ways to prepare the Call Park application for disaster recovery and some considerations for the disaster recovery process.</span></span>

<div>

## <a name="preparing-for-call-park-disaster-recovery"></a><span data-ttu-id="a3e44-107">Preparando-se para a recuperação de desastre do parque da chamada</span><span class="sxs-lookup"><span data-stu-id="a3e44-107">Preparing for Call Park Disaster Recovery</span></span>

<span data-ttu-id="a3e44-108">Lembre-se do seguinte ao se preparar e executar procedimentos de recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="a3e44-108">Keep the following in mind when preparing for and carrying out disaster recovery procedures.</span></span>

  - <span data-ttu-id="a3e44-109">Planeje a recuperação de desastres quando você fizer o planejamento da capacidade.</span><span class="sxs-lookup"><span data-stu-id="a3e44-109">Plan for disaster recovery when you do your capacity planning.</span></span> <span data-ttu-id="a3e44-110">Para a capacidade de recuperação de desastres, cada pool em um pool emparelhado deve ser capaz de manipular as cargas de trabalho dos serviços de estacionamento de chamadas em ambos os pools.</span><span class="sxs-lookup"><span data-stu-id="a3e44-110">For disaster recovery capacity, each pool in a paired pool should be able to handle the workloads of the Call Park services in both pools.</span></span> <span data-ttu-id="a3e44-111">Para obter detalhes sobre o planejamento da capacidade do parque de chamadas, consulte [planejamento de capacidade para estacionamento de chamadas no Lync Server 2013](lync-server-2013-capacity-planning-for-call-park.md).</span><span class="sxs-lookup"><span data-stu-id="a3e44-111">For details about Call Park capacity planning, see [Capacity planning for Call Park in Lync Server 2013](lync-server-2013-capacity-planning-for-call-park.md).</span></span>

  - <span data-ttu-id="a3e44-112">Durante a recuperação de desastres, os usuários que foram redirecionados para o pool de backup como parte do processo de failover usam o serviço de estacionamento de chamadas executado no pool de backup.</span><span class="sxs-lookup"><span data-stu-id="a3e44-112">During disaster recovery, users who have been redirected to the backup pool as part of the failover process use the Call Park service running in the backup pool.</span></span> <span data-ttu-id="a3e44-113">Portanto, o suporte para o parque da chamada durante a recuperação de desastres exige que o aplicativo parque de chamadas seja implantado e habilitado no pool primário e no pool de backup.</span><span class="sxs-lookup"><span data-stu-id="a3e44-113">Therefore, support for Call Park during disaster recovery requires the Call Park application to be deployed and enabled in both the primary pool and the backup pool.</span></span>

  - <span data-ttu-id="a3e44-114">Cada pool deve ter um intervalo válido de números órbitas para usuários que são hospedados nesse pool para usar para chamadas de estacionamento.</span><span class="sxs-lookup"><span data-stu-id="a3e44-114">Each pool must have a valid range of orbit numbers for users who are homed in that pool to use for parking calls.</span></span>

  - <span data-ttu-id="a3e44-115">Mantenha sempre uma cópia de backup separada de qualquer música personalizada em espera que tenha sido carregada para o parque de chamadas.</span><span class="sxs-lookup"><span data-stu-id="a3e44-115">Always keep a separate backup copy of any customized music on hold that has been uploaded for Call Park.</span></span> <span data-ttu-id="a3e44-116">Esses arquivos não são submetidos a backup como parte do processo de recuperação de desastres do Lync Server 2013 e serão perdidos se os arquivos carregados no pool estiverem danificados, corrompidos ou apagados.</span><span class="sxs-lookup"><span data-stu-id="a3e44-116">These files are not backed up as part of the Lync Server 2013 disaster recovery process and will be lost if the files uploaded to the pool are damaged, corrupted, or erased.</span></span>

</div>

<div>

## <a name="call-park-disaster-recovery-considerations"></a><span data-ttu-id="a3e44-117">Considerações sobre a recuperação de desastre do parque</span><span class="sxs-lookup"><span data-stu-id="a3e44-117">Call Park Disaster Recovery Considerations</span></span>

<span data-ttu-id="a3e44-118">Você pode definir apenas um conjunto de configurações de aplicativo de estacionamento de chamada e um arquivo de áudio de música em espera personalizado por pool.</span><span class="sxs-lookup"><span data-stu-id="a3e44-118">You can define only one set of Call Park application configuration settings and one customized music-on-hold audio file per pool.</span></span> <span data-ttu-id="a3e44-119">Essas configurações incluem o limite de tempo limite, música em espera, tentativas máximas de recebimento de chamada e URI de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="a3e44-119">These settings include the timeout threshold, music on hold, maximum call pickup attempts, and timeout URI.</span></span> <span data-ttu-id="a3e44-120">Para exibir essas definições de configuração, execute o cmdlet **Get-CsCpsConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="a3e44-120">To view these configuration settings, run the **Get-CsCpsConfiguration** cmdlet.</span></span> <span data-ttu-id="a3e44-121">Para obter detalhes sobre o cmdlet **Get-CsCpsConfiguration** , consulte [Get-CsCpsConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCpsConfiguration).</span><span class="sxs-lookup"><span data-stu-id="a3e44-121">For details about the **Get-CsCpsConfiguration** cmdlet, see [Get-CsCpsConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCpsConfiguration).</span></span>

<span data-ttu-id="a3e44-122">Durante a recuperação de desastres, o parque de chamadas usa o aplicativo parque de chamadas no pool de backup, portanto, as configurações do pool primário não são incluídas no backup.</span><span class="sxs-lookup"><span data-stu-id="a3e44-122">During disaster recovery, Call Park uses the Call Park application in the backup pool, so settings in the primary pool are not backed up.</span></span> <span data-ttu-id="a3e44-123">Se o pool primário não puder ser recuperado e você implantar um novo pool para substituir o pool primário, as configurações do pool primário serão perdidas, e você precisará reconfigurar as configurações do estacionamento de chamadas e todos os arquivos de áudio de música em espera personalizados no novo pool.</span><span class="sxs-lookup"><span data-stu-id="a3e44-123">If the primary pool can't be recovered and you deploy a new pool to replace the primary pool, the settings from the primary pool are lost, and you need to reconfigure the Call Park settings and any customized music-on-hold audio files in the new pool.</span></span>

<span data-ttu-id="a3e44-124">Se você implantar um novo pool com um nome de domínio totalmente qualificado (FQDN) diferente para substituir o pool primário, será necessário reatribuir todos os intervalos órbitas do parque de chamadas que foram associados ao pool primário ao FQDN do novo pool.</span><span class="sxs-lookup"><span data-stu-id="a3e44-124">If you deploy a new pool with a different fully qualified domain name (FQDN) to replace the primary pool, you need to reassign all the Call Park orbit ranges that were associated with the primary pool to the FQDN of the new pool.</span></span> <span data-ttu-id="a3e44-125">Para reatribuir intervalos de órbita ao novo pool, você pode usar o painel de controle do Lync Server ou o cmdlet **set-CsCallParkOrbit** .</span><span class="sxs-lookup"><span data-stu-id="a3e44-125">To reassign orbit ranges to the new pool, you can use either Lync Server Control Panel or the **Set-CsCallParkOrbit** cmdlet.</span></span> <span data-ttu-id="a3e44-126">Para obter detalhes sobre o cmdlet **set-CsCallParkOrbit** , consulte [set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span><span class="sxs-lookup"><span data-stu-id="a3e44-126">For details about the **Set-CsCallParkOrbit** cmdlet, see [Set-CsCallParkOrbit](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit).</span></span>

<span data-ttu-id="a3e44-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3e44-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

