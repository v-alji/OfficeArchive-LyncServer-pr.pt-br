---
title: Gerenciar as configurações centralizadas de configuração do serviço de log
description: Gerenciar as configurações centralizadas de configuração do serviço de log.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing the Centralized Logging Service configuration settings
ms:assetid: f455c3aa-0061-413d-bdfb-a3e78f82723d
ms:mtpsurl: https://technet.microsoft.com/library/JJ721938(v=OCS.15)
ms:contentKeyID: 49733875
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e25294e096b8368aa06a11e4ad851fe5d1a84c0f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425896"
---
# <a name="managing-the-centralized-logging-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="68910-103">Gerenciar as configurações centralizadas de configuração do serviço de log no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68910-103">Managing the Centralized Logging Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68910-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68910-104">

<span> </span></span></span>

<span data-ttu-id="68910-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="68910-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="68910-106">O serviço de log centralizado é controlado e configurado por configurações e parâmetros que são criados e usados pelo CLSController (Logging Logging Service Controller) para enviar comandos ao agente de serviço de log centralizado do computador individual (CLSAgent).</span><span class="sxs-lookup"><span data-stu-id="68910-106">The Centralized Logging Service is controlled and configured by settings and parameters that are created and used by the Centralized Logging Service Controller (CLSController) to send commands to the individual computer’s Centralized Logging Service Agent (CLSAgent).</span></span> <span data-ttu-id="68910-107">O agente processa os comandos que são enviados a ele e (no caso de um comando Start) usa a configuração dos cenários, provedores, tamanho do log, duração do rastreamento e sinalizadores para começar a coletar logs de rastreamento de acordo com as informações de configuração fornecidas.</span><span class="sxs-lookup"><span data-stu-id="68910-107">The agent processes the commands that are sent to it and (in the case of a Start command) uses the configuration of the scenarios, providers, log size, trace duration, and flags to begin collecting trace logs according to the configuration information provided.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="68910-108">Nem todos os cmdlets do Windows PowerShell listados para o serviço de log centralizado são destinados ao uso com implantações locais do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="68910-108">Not all Windows PowerShell cmdlets listed for the Centralized Logging Service are intended for use with Lync Server 2013 on-premises deployments.</span></span> <span data-ttu-id="68910-109">Embora possam parecer funcionar, os seguintes cmdlets não foram projetados para funcionar com implantações locais do Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="68910-109">Although they may appear to work, the following cmdlets are not designed to function with Lync Server 2013 on-premises deployments:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="68910-110"><STRONG>Cmdlets CsClsRegion:</STRONG> <A href="https://technet.microsoft.com/library/JJ204879(v=OCS.15)">Get-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204746(v=OCS.15)">set-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204658(v=OCS.15)">New-CsClsRegion</A>e <A href="https://technet.microsoft.com/library/JJ204971(v=OCS.15)">Remove-CsClsRegion</A>.</span><span class="sxs-lookup"><span data-stu-id="68910-110"><STRONG>CsClsRegion cmdlets:</STRONG> <A href="https://technet.microsoft.com/library/JJ204879(v=OCS.15)">Get-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204746(v=OCS.15)">Set-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204658(v=OCS.15)">New-CsClsRegion</A>, and <A href="https://technet.microsoft.com/library/JJ204971(v=OCS.15)">Remove-CsClsRegion</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="68910-111"><STRONG>Cmdlets CsClsSearchTerm:</STRONG> <A href="https://technet.microsoft.com/library/JJ205061(v=OCS.15)">Get-CsClsSearchTerm</A> e <A href="https://technet.microsoft.com/library/JJ204911(v=OCS.15)">set-CsClsSearchTerm</A>.</span><span class="sxs-lookup"><span data-stu-id="68910-111"><STRONG>CsClsSearchTerm cmdlets:</STRONG> <A href="https://technet.microsoft.com/library/JJ205061(v=OCS.15)">Get-CsClsSearchTerm</A> and <A href="https://technet.microsoft.com/library/JJ204911(v=OCS.15)">Set-CsClsSearchTerm</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="68910-112"><STRONG>Cmdlets CsClsSecurityGroup:</STRONG> <A href="https://technet.microsoft.com/library/JJ205285(v=OCS.15)">Get-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ204700(v=OCS.15)">set-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ205359(v=OCS.15)">New-CsClsSecurityGroup</A>e <A href="https://technet.microsoft.com/library/JJ204958(v=OCS.15)">Remove-CsClsSecurityGroup</A>.</span><span class="sxs-lookup"><span data-stu-id="68910-112"><STRONG>CsClsSecurityGroup cmdlets:</STRONG> <A href="https://technet.microsoft.com/library/JJ205285(v=OCS.15)">Get-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ204700(v=OCS.15)">Set-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ205359(v=OCS.15)">New-CsClsSecurityGroup</A>, and <A href="https://technet.microsoft.com/library/JJ204958(v=OCS.15)">Remove-CsClsSecurityGroup</A>.</span></span></P></LI></UL><span data-ttu-id="68910-113">As configurações definidas nesses cmdlets não impedirão nem causarão qualquer comportamento adverso, mas serão projetadas para uso com o Microsoft 365 e não produzirão os resultados esperados em implantações locais.</span><span class="sxs-lookup"><span data-stu-id="68910-113">The settings defined in these cmdlets will not hinder or cause any adverse behavior, but they are designed for use with Microsoft 365 and will not yield the expected results in on-premises deployments.</span></span> <span data-ttu-id="68910-114">Isso não quer dizer que não há uso para esses cmdlets em implantações locais, mas sua utilização é um tópico mais avançado, que não é abordado nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="68910-114">This is not to say that there is no use for these cmdlets in on-premises deployments, but their use is a more advanced topic that is not covered in this documentation.</span></span>


</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="68910-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="68910-115">In This Section</span></span>

<span data-ttu-id="68910-116">Os tópicos desta seção definem as opções de configuração, parâmetros e configurações para o serviço de log centralizado.</span><span class="sxs-lookup"><span data-stu-id="68910-116">The topics in this section define the configuration options, parameters, and settings for the Centralized Logging Service.</span></span> <span data-ttu-id="68910-117">Informações sobre como configurar o serviço de log centralizado, como recuperar as definições de configuração, a criação de cenários, o gerenciamento de grupos de segurança para o serviço de log centralizado, a pesquisa e outros recursos estão contidos nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="68910-117">Information about how to configure the Centralized Logging Service, how to retrieve the configuration settings, creation of scenarios, management of security groups for Centralized Logging Service, searching, and more is contained in the following topics.</span></span>

  - [<span data-ttu-id="68910-118">Gerenciando o computador, o site e a configuração de serviço de log centralizado global no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68910-118">Managing computer, site and global Centralized Logging Service configuration in Lync Server 2013</span></span>](lync-server-2013-managing-computer-site-and-global-centralized-logging-service-configuration.md)

  - [<span data-ttu-id="68910-119">Configurando provedores para o serviço de log centralizado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68910-119">Configuring providers for Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-configuring-providers-for-centralized-logging-service.md)

  - [<span data-ttu-id="68910-120">Configurar cenários para o serviço de log centralizado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68910-120">Configuring scenarios for the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-configuring-scenarios-for-the-centralized-logging-service.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="68910-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="68910-121">See Also</span></span>


[<span data-ttu-id="68910-122">Visão geral do serviço de log centralizado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68910-122">Overview of the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-centralized-logging-service.md)  
[<span data-ttu-id="68910-123">Cmdlets de log centralizado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68910-123">Centralized Logging cmdlets in Lync Server 2013</span></span>](lync-server-2013-centralized-logging-cmdlets.md)  
  

<span data-ttu-id="68910-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68910-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

