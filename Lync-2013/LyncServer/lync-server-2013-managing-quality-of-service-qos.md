---
title: 'Lync Server 2013: Gerenciando a qualidade do serviço (QoS)'
description: 'Lync Server 2013: Gerenciando a qualidade do serviço (QoS).'
ms.reviewer: ''
f1.keywords:
- NOCSH
TOCTitle: Managing Quality of Service (QoS)
author: lanachin
ms.author: v-lanac
ms.manager: serdars
ms:assetid: ab1051c3-8380-4d72-86df-37a61b1e4a41
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg405409(v=OCS.15)
ms:contentKeyID: 48185049
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: df0e84389cc030cd63fe04c46929bd981a074aec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437277"
---
# <a name="managing-quality-of-service-qos-in-lync-server-2013"></a><span data-ttu-id="75a33-103">Gerenciando a qualidade do serviço (QoS) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="75a33-103">Managing Quality of Service (QoS) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="75a33-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="75a33-104">

<span> </span></span></span>

<span data-ttu-id="75a33-105">_**Tópico da última modificação:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="75a33-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="75a33-106">A QoS (qualidade de serviço) é uma tecnologia de rede usada em algumas organizações para ajudar a oferecer uma experiência ideal para o usuário final para comunicações de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="75a33-106">Quality of Service (QoS) is a networking technology used in some organizations to help provide an optimal end-user experience for audio and video communications.</span></span> <span data-ttu-id="75a33-107">A QoS é mais comumente usada em redes em que a largura de banda é limitada: com um grande número de pacotes de rede competindo por uma quantidade relativamente pequena de largura de banda disponível, a qualidade do serviço fornece uma maneira para os administradores atribuirem prioridades maiores aos pacotes que transportam dados de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="75a33-107">QoS is most-commonly used on networks where bandwidth is limited: with a large number of network packets competing for a relatively small amount of available bandwidth, Quality of Service provides a way for administrators to assign higher priorities to packets carrying audio or video data.</span></span> <span data-ttu-id="75a33-108">Ao fornecer esses pacotes, é provável que as comunicações de áudio e vídeo sejam concluídas com mais rapidez e menos interrupções do que as sessões de rede envolvendo itens como transferências de arquivos, navegação na Web ou backups de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="75a33-108">By giving these packets a higher priority, audio and video communications are likely to complete faster, and with less interruption, than network sessions involving things like file transfers, web browsing, or database backups.</span></span> <span data-ttu-id="75a33-109">Isso ocorre porque os pacotes de rede usados para transferências de arquivos ou backups de bancos de dados recebem uma atribuição de prioridade de "melhor esforço".</span><span class="sxs-lookup"><span data-stu-id="75a33-109">That's because network packets used for file transfers or database backups are assigned a "best effort" priority.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="75a33-110">Como regra geral, a qualidade do serviço aplica-se somente a sessões de comunicação em sua rede interna.</span><span class="sxs-lookup"><span data-stu-id="75a33-110">As a general rule, Quality of Service applies only to communication sessions on your internal network.</span></span> <span data-ttu-id="75a33-111">Ao implementar QoS, você configura seus servidores e roteadores para dar suporte à marcação de pacotes; no entanto, você configura esses dispositivos para dar suporte à marcação de pacotes de uma maneira específica.</span><span class="sxs-lookup"><span data-stu-id="75a33-111">When you implement QoS, you configure your servers and routers to support packet marking; however, you configure these devices to support packet marking in a particular manner.</span></span> <span data-ttu-id="75a33-112">Você não pode supor que a qualidade do serviço será compatível na Internet ou em outras redes.</span><span class="sxs-lookup"><span data-stu-id="75a33-112">You cannot assume that Quality of Service will be supported on the Internet or on other networks.</span></span> <span data-ttu-id="75a33-113">Mesmo que o serviço de qualidade seja compatível com outras redes, não há garantia de que a QoS será configurada da mesma maneira que você configurou o serviço na sua rede.</span><span class="sxs-lookup"><span data-stu-id="75a33-113">Even if Quality if Service is supported on other networks, there is no guarantee that QoS will be configured the same way that you configured the service on your network.</span></span>



</div>

<span data-ttu-id="75a33-114">O Microsoft Lync Server 2013 não requer qualidade de serviço; Se você não usa o QoS no momento, não há necessidade de instalar o serviço antes de instalar o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="75a33-114">Microsoft Lync Server 2013 does not require Quality of Service; if you do not currently use QoS there is no requirement that you install the service before installing Lync Server 2013.</span></span> <span data-ttu-id="75a33-115">Se você tiver uma quantidade considerável de perda de pacotes na rede, a maneira recomendada de aliviar esse problema é adicionar mais largura de banda.</span><span class="sxs-lookup"><span data-stu-id="75a33-115">If you experience a considerable amount of packet loss on your network the recommended way to alleviate this problem is to add additional bandwidth.</span></span> <span data-ttu-id="75a33-116">Se não for possível adicionar mais largura de banda, talvez você queira implementar a qualidade do serviço em vez disso.</span><span class="sxs-lookup"><span data-stu-id="75a33-116">If adding more bandwidth is not possible, then you might want to implement Quality of Service instead.</span></span>

<span data-ttu-id="75a33-117">O Lync Server 2013 oferece suporte completo para a qualidade do serviço: isso significa que as organizações que já estão usando a QoS podem integrar facilmente o Lync Server à sua infraestrutura de rede existente.</span><span class="sxs-lookup"><span data-stu-id="75a33-117">Lync Server 2013 offers full support for Quality of Service: that means that organizations that are already using QoS can easily integrate Lync Server into their existing network infrastructure.</span></span> <span data-ttu-id="75a33-118">Para fazer isso, você deve executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="75a33-118">In order to do this you must perform the following tasks:</span></span>

  - <span data-ttu-id="75a33-119">[Habilitando a QoS no Lync Server 2013 para dispositivos que não são baseados no Windows](lync-server-2013-enabling-qos-for-devices-that-are-not-based-on-windows.md).</span><span class="sxs-lookup"><span data-stu-id="75a33-119">[Enabling QoS in Lync Server 2013 for devices that are not based on Windows](lync-server-2013-enabling-qos-for-devices-that-are-not-based-on-windows.md).</span></span> <span data-ttu-id="75a33-120">Por padrão, a QoS é desativada em computadores e outros dispositivos (como iPhones) que executam outros sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="75a33-120">By default, QoS is disabled for computers and other devices (such as iPhones) that run other operating systems.</span></span> <span data-ttu-id="75a33-121">Embora você possa usar o Lync Server para habilitar e desabilitar a qualidade do serviço para dispositivos, normalmente não é possível usar o produto para modificar os códigos DSCP usados por esses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="75a33-121">Although you can use Lync Server to enable and disable Quality of Service for devices, you typically cannot use the product to modify the DSCP codes used by these devices.</span></span>

  - <span data-ttu-id="75a33-122">[Configurar intervalos de porta no Lync Server 2013 para servidores de conferência, aplicativo e mediação](lync-server-2013-configuring-port-ranges-for-your-conferencing-application-and-mediation-servers.md).</span><span class="sxs-lookup"><span data-stu-id="75a33-122">[Configuring port ranges in Lync Server 2013 for your Conferencing, Application, and Mediation servers](lync-server-2013-configuring-port-ranges-for-your-conferencing-application-and-mediation-servers.md).</span></span> <span data-ttu-id="75a33-123">É necessário reservar um conjunto exclusivo de portas para tipos de pacotes diferentes, como áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="75a33-123">You must reserve a unique set of ports for different packet types, such as audio and video.</span></span> <span data-ttu-id="75a33-124">Com o Lync Server 2013, você não habilita ou desabilita a qualidade do serviço por, digamos, definir um valor de propriedade como verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="75a33-124">With Lync Server 2013 you do not enable or disable Quality of Service by, say, setting a property value to True or to False.</span></span> <span data-ttu-id="75a33-125">Em vez disso, habilite a qualidade de serviço Configurando intervalos de porta e, em seguida, criando e aplicando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="75a33-125">Instead, you enable Quality of Service by configuring port ranges and then creating and applying Group Policy.</span></span> <span data-ttu-id="75a33-126">Se, mais tarde, você decidir não usar o QoS, poderá "Desabilitar" a qualidade do serviço simplesmente removendo os objetos de política de grupo apropriados.</span><span class="sxs-lookup"><span data-stu-id="75a33-126">If you later decide not to use QoS you can “disable” Quality of Service simply by removing the appropriate Group Policy objects.</span></span>

  - <span data-ttu-id="75a33-127">[Configurando intervalos de porta para seus servidores de borda no Lync Server 2013](lync-server-2013-configuring-port-ranges-for-your-edge-servers.md).</span><span class="sxs-lookup"><span data-stu-id="75a33-127">[Configuring port ranges for your Edge Servers in Lync Server 2013](lync-server-2013-configuring-port-ranges-for-your-edge-servers.md).</span></span> <span data-ttu-id="75a33-128">Embora não seja necessário, você pode configurar seus servidores de borda para usar os mesmos intervalos de porta que os outros servidores.</span><span class="sxs-lookup"><span data-stu-id="75a33-128">Although not required, you can configure your Edge servers to use the same port ranges as your other servers.</span></span>

  - <span data-ttu-id="75a33-129">[Configurar intervalos de porta para seus clientes do Microsoft Lync no Lync Server 2013](lync-server-2013-configuring-port-ranges-for-your-microsoft-lync-clients.md).</span><span class="sxs-lookup"><span data-stu-id="75a33-129">[Configuring port ranges for your Microsoft Lync clients in Lync Server 2013](lync-server-2013-configuring-port-ranges-for-your-microsoft-lync-clients.md).</span></span> <span data-ttu-id="75a33-130">Esses intervalos de porta se aplicam apenas aos computadores cliente e são tipicamente diferentes dos intervalos de porta configurados em seus servidores.</span><span class="sxs-lookup"><span data-stu-id="75a33-130">These port ranges apply only to client computers and are typically not the same as the port ranges configured on your servers.</span></span>

  - <span data-ttu-id="75a33-131">[Configurar uma política de qualidade de serviço no Lync Server 2013 para servidores de conferência, aplicativo e mediação](lync-server-2013-configuring-a-quality-of-service-policy-for-your-conferencing-application-and-mediation-servers.md).</span><span class="sxs-lookup"><span data-stu-id="75a33-131">[Configuring a Quality of Service policy in Lync Server 2013 for your Conferencing, Application, and Mediation servers](lync-server-2013-configuring-a-quality-of-service-policy-for-your-conferencing-application-and-mediation-servers.md).</span></span> <span data-ttu-id="75a33-132">Essas políticas determinam os códigos DSCP aplicados a diferentes tipos de pacote.</span><span class="sxs-lookup"><span data-stu-id="75a33-132">These policies determine the DSCP codes that are applied to different packet types.</span></span>

  - <span data-ttu-id="75a33-133">[Configurar uma política de qualidade de serviço para seus servidores de borda a/V no Lync Server 2013](lync-server-2013-configuring-a-quality-of-service-policy-for-your-a-v-edge-servers.md).</span><span class="sxs-lookup"><span data-stu-id="75a33-133">[Configuring a Quality of Service policy for your A/V Edge Servers in Lync Server 2013](lync-server-2013-configuring-a-quality-of-service-policy-for-your-a-v-edge-servers.md).</span></span> <span data-ttu-id="75a33-134">Isso deve ser executado somente para o lado interno de seus servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="75a33-134">This should only be done for the internal side of your Edge servers.</span></span> <span data-ttu-id="75a33-135">Isso porque a qualidade do serviço foi projetada para ser usada em sua rede interna e não na Internet.</span><span class="sxs-lookup"><span data-stu-id="75a33-135">That's because Quality of Service is designed for use on your internal network and not on the Internet.</span></span>

  - <span data-ttu-id="75a33-136">[Configuração de políticas de qualidade de serviço no Lync Server 2013 para clientes em execução no Windows 7 ou no Windows 8](lync-server-2013-configuring-quality-of-service-policies-for-clients-running-on-windows-7-or-windows-8.md).</span><span class="sxs-lookup"><span data-stu-id="75a33-136">[Configuring Quality of Service policies in Lync Server 2013 for clients running on Windows 7 or Windows 8](lync-server-2013-configuring-quality-of-service-policies-for-clients-running-on-windows-7-or-windows-8.md).</span></span> <span data-ttu-id="75a33-137">Observe que o Microsoft Lync Server 2013 não é compatível com QoS para outros sistemas operacionais Windows, como Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="75a33-137">Note that Microsoft Lync Server 2013 does not support QoS for other Windows operating systems, such as Windows Vista or Windows XP.</span></span>

  - <span data-ttu-id="75a33-138">[Configurando a qualidade do serviço em dispositivos Microsoft Lync Phone Edition no Lync Server 2013](lync-server-2013-configuring-quality-of-service-on-microsoft-lync-phone-edition-devices.md).</span><span class="sxs-lookup"><span data-stu-id="75a33-138">[Configuring Quality of Service on Microsoft Lync Phone Edition devices in Lync Server 2013](lync-server-2013-configuring-quality-of-service-on-microsoft-lync-phone-edition-devices.md).</span></span> <span data-ttu-id="75a33-139">Por padrão, a QoS está habilitada para dispositivos do Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="75a33-139">By default, QoS is enabled for Lync Phone Edition devices.</span></span> <span data-ttu-id="75a33-140">No entanto, talvez você queira alterar o valor padrão de DSCP para garantir que todos os pacotes de áudio em sua organização usem o mesmo código DSCP.</span><span class="sxs-lookup"><span data-stu-id="75a33-140">However, you might want to change the default DSCP value in order to ensure that all audio packets in your organization use the same DSCP code.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="75a33-141">Se você estiver usando o Microsoft Windows Server 2012 ou o Windows Server 2012 R2, talvez esteja interessado no novo conjunto de cmdlets do Windows PowerShell disponíveis para o gerenciamento da qualidade do serviço nessa plataforma.</span><span class="sxs-lookup"><span data-stu-id="75a33-141">If you are using Microsoft Windows Server 2012 or Windows Server 2012 R2 you might be interested in the new set of Windows PowerShell cmdlets available for managing Quality of Service on that platform.</span></span> <span data-ttu-id="75a33-142">Para obter mais informações, consulte cmdlets de qualidade de serviço de rede no Windows PowerShell em [https://docs.microsoft.com/powershell/module/netqos/?view=winserver2012-ps](https://docs.microsoft.com/powershell/module/netqos/?view=winserver2012-ps) .</span><span class="sxs-lookup"><span data-stu-id="75a33-142">For more information, see Network Quality of Service Cmdlets in Windows PowerShell at [https://docs.microsoft.com/powershell/module/netqos/?view=winserver2012-ps](https://docs.microsoft.com/powershell/module/netqos/?view=winserver2012-ps).</span></span>



<span data-ttu-id="75a33-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="75a33-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

