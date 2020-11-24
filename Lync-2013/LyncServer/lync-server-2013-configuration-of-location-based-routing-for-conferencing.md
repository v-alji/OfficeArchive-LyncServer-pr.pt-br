---
title: 'Lync Server 2013: Configuração do Roteamento Baseado em Local para conferência'
description: 'Lync Server 2013: configuração do roteamento Location-Based para conferência.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390372"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="3db19-103">Configuração do Roteamento Baseado em Local para conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3db19-103">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3db19-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3db19-104">

<span> </span></span></span>

<span data-ttu-id="3db19-105">_**Tópico da última modificação:** 2013-09-11_</span><span class="sxs-lookup"><span data-stu-id="3db19-105">_**Topic Last Modified:** 2013-09-11_</span></span>

<span data-ttu-id="3db19-106">O aplicativo de conferência de roteamento Location-Based depende da configuração do Lync Server 2013 Location-Based Routing.</span><span class="sxs-lookup"><span data-stu-id="3db19-106">The Location-Based Routing Conferencing application relies on the configuration of Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="3db19-107">Estas são as principais configurações:</span><span class="sxs-lookup"><span data-stu-id="3db19-107">The main configurations are the following:</span></span>

  - <span data-ttu-id="3db19-108">O local dos participantes que ingressam em uma reunião é determinado com base em seus locais de rede.</span><span class="sxs-lookup"><span data-stu-id="3db19-108">The location of participants joining a meeting is determined based on their network site.</span></span> <span data-ttu-id="3db19-109">Um site de rede e suas sub-redes de rede associadas devem ser definidos no Lync Server para impor Location-Based roteamento.</span><span class="sxs-lookup"><span data-stu-id="3db19-109">A network site and its associated network subnets must be defined in Lync Server in order to enforce Location-Based Routing.</span></span>

  - <span data-ttu-id="3db19-110">Para aplicar Location-Based roteamento de reuniões, os participantes do Lync devem ser habilitados para Location-Based roteamento.</span><span class="sxs-lookup"><span data-stu-id="3db19-110">To enforce Location-Based Routing of meetings, Lync participants must be enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="3db19-111">Para aplicar Location-Based roteamento de pontos de extremidade PSTN ingressando em reuniões, o tronco SIP usado para conectar os pontos de extremidade PSTN devem ser configurados para Location-Based roteamento.</span><span class="sxs-lookup"><span data-stu-id="3db19-111">To enforce Location-Based Routing of PSTN endpoints joining meetings, the SIP trunk used to connect the PSTN endpoints must be configured for Location-Based Routing.</span></span>

<span data-ttu-id="3db19-112">Para obter informações adicionais sobre como implantar e configurar o roteamento Location-Based do Lync Server 2013, consulte Configurando o [roteamento baseado em local](lync-server-2013-configuring-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="3db19-112">For additional information on deploying and configuring Lync Server 2013 Location-Based Routing, please refer Configuring [Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a><span data-ttu-id="3db19-113">Habilitando o aplicativo de conferência de roteamento de Location-Based</span><span class="sxs-lookup"><span data-stu-id="3db19-113">Enabling the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="3db19-114">O aplicativo de conferência de roteamento Location-Based está desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="3db19-114">The Location-Based Routing Conferencing application is disabled by default.</span></span> <span data-ttu-id="3db19-115">Antes de habilitá-lo, determine a prioridade certa para atribuir a ele.</span><span class="sxs-lookup"><span data-stu-id="3db19-115">Before enabling this application, you need to determine the right priority to assign for the application.</span></span> <span data-ttu-id="3db19-116">Para determinar essa prioridade, execute o seguinte cmdlet no Shell de gerenciamento do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="3db19-116">To determine this priority, run the following cmdlet in Lync Server Management Shell:</span></span>

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

<span data-ttu-id="3db19-117">Nesse cmdlet, \<Pool FQDN\> é o pool no qual o aplicativo de conferência de roteamento Location-Based está habilitado.</span><span class="sxs-lookup"><span data-stu-id="3db19-117">In this cmdlet, \<Pool FQDN\> is the pool in which the Location-Based Routing Conferencing application is to be enabled.</span></span>

<span data-ttu-id="3db19-118">Esse cmdlet retornará a lista dos aplicativos hospedados pelo Lync Server e o valor de prioridade para cada um deles.</span><span class="sxs-lookup"><span data-stu-id="3db19-118">This cmdlet will return the list of the applications hosted by Lync Server and the priority value for each of them.</span></span> <span data-ttu-id="3db19-119">O aplicativo de conferência de roteamento Location-Based precisa ser atribuído um valor de prioridade maior do que o aplicativo "UdcAgent" e menor do que os aplicativos "defaultrouting", "ExumRouting" e "OutboundRouting".</span><span class="sxs-lookup"><span data-stu-id="3db19-119">The Location-Based Routing Conferencing application needs to be assigned a priority value larger than the “UdcAgent” application and smaller than the “DefaultRouting”, “ExumRouting” and “OutboundRouting” applications.</span></span> <span data-ttu-id="3db19-120">Recomendamos que você atribua o aplicativo de videoconferência Location-Based um valor de prioridade que seja um ponto maior do que o valor de prioridade do aplicativo "UdcAgent".</span><span class="sxs-lookup"><span data-stu-id="3db19-120">We recommend that you assign the Location-Based Routing Conferencing application a priority value that is one point higher than the priority value of the “UdcAgent” application.</span></span>

<span data-ttu-id="3db19-121">Por exemplo, se o aplicativo "UdcAgent" tem um valor de prioridade "2", o aplicativo "defaultrouting" tem um valor de prioridade de "8", o aplicativo "ExumRouting" tem um valor de prioridade de "9" e o aplicativo "OutboundRouting" tem um valor de prioridade de "10", então você deve atribuir o aplicativo de videoconferência Location-Based um valor de prioridade "3"</span><span class="sxs-lookup"><span data-stu-id="3db19-121">For example, if the “UdcAgent” application has a priority value of “2”, the “DefaultRouting” application has a priority value of “8”, the “ExumRouting” application has a priority value of “9” and the “OutboundRouting” application has a priority value of “10” then you should assign the Location-Based Routing Conferencing application a priority value of “3”.</span></span> <span data-ttu-id="3db19-122">Isso colocaria a prioridade dos aplicativos na seguinte ordem: outros aplicativos (prioridades: de 0 a 1), "UdcAgent" (prioridade: 2), Location-Based aplicativo de conferência de roteamento (prioridade: 3), outros aplicativos (prioridades: 4 a 8), "defaultrouting" (prioridade: 9), "ExumRouting" (prioridade: 10) e "OutboundRouting" (prioridade: 11)</span><span class="sxs-lookup"><span data-stu-id="3db19-122">Doing so would place the priority of the applications in the following order: Other applications (Priorities: 0 to 1), “UdcAgent” (Priority: 2), Location-Based Routing Conferencing application (Priority: 3), other applications (Priorities: 4 to 8), “DefaultRouting” (Priority: 9), “ExumRouting” (Priority: 10) and “OutboundRouting” (Priority: 11).</span></span>

<span data-ttu-id="3db19-123">Depois de encontrar o valor de prioridade correto para o aplicativo de videoconferência de Location-Based, digite o seguinte cmdlet para cada servidor de Front-End pool ou Standard Edition que os usuários habilitarem para o roteamento Location-Based:</span><span class="sxs-lookup"><span data-stu-id="3db19-123">After you find the correct priority value for the Location-Based Routing Conferencing application, type the following cmdlet for each Front-End pool or Standard Edition Server that homes users enabled for Location-Based Routing:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="3db19-124">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3db19-124">For example:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="3db19-125">Depois de usar esse cmdlet, reinicie todos os servidores front-end no pool ou os servidores Standard Edition nos quais o aplicativo de audioconferência Location-Based está habilitado.</span><span class="sxs-lookup"><span data-stu-id="3db19-125">After using this cmdlet, restart all Front End servers in the pool or the Standard Edition Servers where the Location-Based Routing Conferencing application has been enabled.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3db19-126">Location-Based os enforcementos de roteamento para conferências ou transferências consuldas não serão impostos até que todos os servidores de front-end nos pools aplicáveis ou servidores padrão da edição sejam reiniciados.</span><span class="sxs-lookup"><span data-stu-id="3db19-126">Location-Based Routing enforcements to conferences or consultative transfers won’t be enforced until all the Front End Servers in the applicable pools or the Standard Edition Servers are restarted.</span></span>



</div>

<span data-ttu-id="3db19-127">Depois que o aplicativo de conferência de roteamento Location-Based foi habilitado com êxito e todos os servidores de Lync aplicáveis foram reiniciados, todas as conferências organizadas pelos usuários do Lync habilitados para Location-Based roteamento serão monitoradas para evitar a interligação PSTN em desvio</span><span class="sxs-lookup"><span data-stu-id="3db19-127">Once the Location-Based Routing Conferencing application has been successfully enabled and all applicable Lync servers have been restarted, all conferences organized by Lync users enabled for Location-Based Routing will be monitored to prevent PSTN toll bypass</span></span>

<span data-ttu-id="3db19-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3db19-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

