---
title: 'Lync Server 2013: instalando os pacotes de gerenciamento do Lync Server 2013'
description: 'Lync Server 2013: instalando os pacotes de gerenciamento do Lync Server 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: nstalling the Lync Server 2013 management packs
ms:assetid: b800d4ab-fdc8-4c72-a76a-b78932779fe3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205202(v=OCS.15)
ms:contentKeyID: 48185233
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cbb50146474211c12dbd95801ed2b20f6bbfd8c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426925"
---
# <a name="installing-the-lync-server-2013-management-packs"></a><span data-ttu-id="e9a07-103">Instalar os pacotes de gerenciamento do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e9a07-103">Installing the Lync Server 2013 management packs</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9a07-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9a07-104">

<span> </span></span></span>

<span data-ttu-id="e9a07-105">_**Tópico da última modificação:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="e9a07-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="e9a07-106">Por si só, o System Center Operations Manager tem a capacidade de monitorar apenas uma pequena parte do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="e9a07-106">By itself, System Center Operations Manager has the ability to monitor only a small portion of the Windows operating system.</span></span> <span data-ttu-id="e9a07-107">No entanto, você pode estender os recursos do System Center Operations Manager, Instalando pacotes de gerenciamento, que determinam quais itens o System Center Operations Manager pode monitorar, incluindo como esses itens devem ser monitorados e como os alertas devem ser acionados e relatados.</span><span class="sxs-lookup"><span data-stu-id="e9a07-107">However, you can extend the capabilities of System Center Operations Manager by installing management packs, software that dictates which items System Center Operations Manager can monitor, including how those items should be monitored and how alerts should be triggered and reported.</span></span> <span data-ttu-id="e9a07-108">O Microsoft Lync Server 2013 inclui dois pacotes de gerenciamento do System Center Operations Manager que fornecem os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="e9a07-108">Microsoft Lync Server 2013 includes two System Center Operations Manager management packs that provide the following capabilities:</span></span>

  - <span data-ttu-id="e9a07-109">O componente e o pacote de gerenciamento de usuários (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) controla problemas do Lync Server gravados em logs de eventos, registrados por contadores de desempenho, ou registrados nos bancos de dados de registros de detalhes de chamadas (CDR) ou na Quality of Experience (QoE).</span><span class="sxs-lookup"><span data-stu-id="e9a07-109">The Component and User Management Pack (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) tracks Lync Server issues recorded in event logs, registered by performance counters, or logged in the call detail records (CDR) or the Quality of Experience (QoE) databases.</span></span> <span data-ttu-id="e9a07-110">Para problemas críticos, o System Center Operations Manager pode ser configurado para notificar imediatamente os administradores por email, mensagem instantânea ou mensagens SMS (serviço de mensagens curtas).</span><span class="sxs-lookup"><span data-stu-id="e9a07-110">For critical problems, System Center Operations Manager can be configured to immediately notify administrators via email, instant message, or Short Message Service (SMS) messaging.</span></span> <span data-ttu-id="e9a07-111">SMS é a tecnologia usada para enviar mensagens de texto de um dispositivo móvel para outro.</span><span class="sxs-lookup"><span data-stu-id="e9a07-111">SMS is the technology used to send text messages from one mobile device to another.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e9a07-112">Para obter mais informações sobre como configurar a notificação do Operations Manager, consulte Configurando a notificação na biblioteca do TechNet em <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?linkid=268785</A> .</span><span class="sxs-lookup"><span data-stu-id="e9a07-112">For more information on configuring Operations Manager notification, see Configuring Notification in the TechNet Library at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?linkid=268785</A>.</span></span>

    
    </div>

  - <span data-ttu-id="e9a07-113">O pacote de monitoramento ativo (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) testa proativamente os principais componentes do Lync Server, como fazer logon no sistema, trocar mensagens instantâneas ou fazer chamadas para um telefone localizado na rede telefônica pública comutada (PSTN).</span><span class="sxs-lookup"><span data-stu-id="e9a07-113">The Active Monitoring Pack (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) proactively tests key Lync Server components such as logging on to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="e9a07-114">Esses testes são conduzidos usando cmdlets de transação sintéticas do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e9a07-114">These tests are conducted using the Lync Server synthetic transaction cmdlets.</span></span> <span data-ttu-id="e9a07-115">Por exemplo, o cmdlet **Test-CsIM** é usado para simular uma conversa de mensagens instantâneas entre um par de usuários de teste.</span><span class="sxs-lookup"><span data-stu-id="e9a07-115">For example, the **Test-CsIM** cmdlet is used to simulate an instant messaging conversation between a pair of test users.</span></span> <span data-ttu-id="e9a07-116">Se essa conversa de mensagens simulada falhar, um alerta será gerado.</span><span class="sxs-lookup"><span data-stu-id="e9a07-116">If this simulated messaging conversation fails an alert will be generated.</span></span>

<span data-ttu-id="e9a07-117">Os dois pacotes de gerenciamento incluídos no Lync Server 2013 incluem uma grande quantidade de aprimoramentos nos pacotes de gerenciamento usados com o Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="e9a07-117">The two management packs included with Lync Server 2013 include a large number of enhancements over the management packs used with Microsoft Lync Server 2010.</span></span> <span data-ttu-id="e9a07-118">Por exemplo, o pacote de gerenciamento do componente do Lync Server 2013 não está limitado ao monitoramento próprio do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e9a07-118">For example, the Lync Server 2013 Component Management Pack is not limited to monitoring Lync Server itself.</span></span> <span data-ttu-id="e9a07-119">Além de monitorar os logs de eventos e os contadores de desempenho do Lync Server, o pacote de gerenciamento de componentes também pode controlar o desempenho de itens cruciais e emitir alertas para itens cruciais, como:</span><span class="sxs-lookup"><span data-stu-id="e9a07-119">In addition to monitoring event logs and performance counters for Lync Server, the Component Management pack can also track the performance of, and issue alerts for, crucial items such as:</span></span>

  - <span data-ttu-id="e9a07-120">**Serviços de informações da Internet (IIS)**   Alertas serão emitidos se os serviços de informações da Internet ficarão offline.</span><span class="sxs-lookup"><span data-stu-id="e9a07-120">**Internet Information Services (IIS)**   Alerts will be issued if Internet Information Services goes offline.</span></span> <span data-ttu-id="e9a07-121">Isso é importante, pois os serviços Web do Lync Server dependem do IIS.</span><span class="sxs-lookup"><span data-stu-id="e9a07-121">This is important, because the Lync Server web services rely on IIS.</span></span>

  - <span data-ttu-id="e9a07-122">**Uso do processo**   Os alertas serão emitidos se os recursos do sistema (como memória disponível) começarem a ficar baixos.</span><span class="sxs-lookup"><span data-stu-id="e9a07-122">**Process usage**   Alerts will be issued if system resources (such as available memory) begin to run low.</span></span> <span data-ttu-id="e9a07-123">Esses alertas serão emitidos mesmo se o Lync Server não for responsável pelo alto uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="e9a07-123">These alerts will be issued even if Lync Server is not responsible for the high system usage.</span></span>

  - <span data-ttu-id="e9a07-124">**Eventos de falha do computador**   Os alertas serão emitidos em caso de um problema de hardware ou software que ameaça a viabilidade de um servidor.</span><span class="sxs-lookup"><span data-stu-id="e9a07-124">**Computer failure events**   Alerts will be issued in case of a hardware or software issue that threatens the viability of a server.</span></span> <span data-ttu-id="e9a07-125">Por exemplo, os administradores do Lync Server serão notificados se um servidor parecer estar em perigo de ocorrer uma falha no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="e9a07-125">For example, Lync Server administrators will be notified if a server appears to be in danger of experiencing a hard disk failure.</span></span>

<span data-ttu-id="e9a07-126">Os novos pacotes de gerenciamento também apresentam relatórios avançados.</span><span class="sxs-lookup"><span data-stu-id="e9a07-126">The new management packs also feature enhanced reporting.</span></span> <span data-ttu-id="e9a07-127">Os novos relatórios do Lync Server 2013 incluem:</span><span class="sxs-lookup"><span data-stu-id="e9a07-127">New reports for Lync Server 2013 include:</span></span>

  - <span data-ttu-id="e9a07-128">**Relatório de disponibilidade de cenário de ponta a ponta**   Esse relatório detalha a disponibilidade/tempo de atividade para os principais serviços do Lync Server, como registro ou presença.</span><span class="sxs-lookup"><span data-stu-id="e9a07-128">**End to End Scenario Availability Report**   This report details the availability/uptime for key Lync Server services such as registration or presence.</span></span>

  - <span data-ttu-id="e9a07-129">**Relatório de capacidade**   Usando informações de contador de desempenho, esse relatório mostra tendências para componentes do sistema, como disponibilidade da memória e uso do processador.</span><span class="sxs-lookup"><span data-stu-id="e9a07-129">**Capacity Report**   Using performance counter information, this report shows trends for system components such as memory availability and processor usage.</span></span>

  - <span data-ttu-id="e9a07-130">**Relatório de componente**   Esse relatório lista os principais geradores de alertas agrupados pelo componente do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e9a07-130">**Component Report**   This report lists the top alert generators grouped by Lync Server component.</span></span>

<span data-ttu-id="e9a07-131">Além desses relatórios predefinidos, os pacotes de gerenciamento do Lync Server 2013 automaticamente relatam alertas para a confiabilidade das chamadas (métricas medidas por gravação de detalhes de chamadas) e Estados de QoE (métricas medidas por qualidade de experiência).</span><span class="sxs-lookup"><span data-stu-id="e9a07-131">In addition to these predesigned reports, the management packs for Lync Server 2013 automatically report alerts for both Call Reliability (metrics measured by Call Detail Recording) and QoE states (metrics measured by Quality of Experience).</span></span> <span data-ttu-id="e9a07-132">Se você tiver habilitado a gravação de detalhes da chamada, poderá revisar os alertas de confiabilidade da chamada completando o procedimento a seguir no console do System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="e9a07-132">If you have enabled Call Detail Recording, you can review Call Reliability alerts by completing the following procedure from the System Center Operations Manager console:</span></span>

  - <span data-ttu-id="e9a07-133">Expanda **monitoramento**, expanda **integridade do Microsoft Lync Server 2013**, expanda a **confiabilidade da chamada e a qualidade da mídia** e clique em **chamar confiabilidade**.</span><span class="sxs-lookup"><span data-stu-id="e9a07-133">Expand **Monitoring**, expand **Microsoft Lync Server 2013 Health**, expand **Call Reliability and Media Quality**, and then click **Call Reliability**.</span></span>

<span data-ttu-id="e9a07-134">Para ver os alertas de qualidade da experiência, conclua este procedimento no console do System Center Operations Manager:</span><span class="sxs-lookup"><span data-stu-id="e9a07-134">To view Quality of Experience alerts, complete this procedure from the System Center Operations Manager console:</span></span>

  - <span data-ttu-id="e9a07-135">Expanda **monitoramento**, expanda **integridade do Microsoft Lync Server 2013**, expanda a **confiabilidade da chamada e a qualidade da mídia** e expanda qualidade da **mídia**.</span><span class="sxs-lookup"><span data-stu-id="e9a07-135">Expand **Monitoring**, expand **Microsoft Lync Server 2013 Health**, expand **Call Reliability and Media Quality**, and then expand **Media Quality**.</span></span>

<span data-ttu-id="e9a07-136">Os pacotes de gerenciamento do Lync Server 2013 agora usam a descoberta em nível de máquina em vez do mecanismo de descoberta central usado no Microsoft Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="e9a07-136">The management packs for Lync Server 2013 now use machine-level discovery instead of the central discovery mechanism used in Microsoft Lync Server 2010.</span></span> <span data-ttu-id="e9a07-137">Isso significa que cada agente do System Center essencialmente descobre e relata sua existência ao servidor central de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="e9a07-137">This means that each System Center agent essentially discovers itself and reports its existence to the Central Management Server.</span></span> <span data-ttu-id="e9a07-138">O uso da descoberta no nível da máquina simplifica a administração da infraestrutura do System Center e também permite diferentes versões dos pacotes de gerenciamento do Lync Server (por exemplo, pacotes de gerenciamento do Lync Server 2010 e pacotes de gerenciamento do Lync Server 2013) para coexistência.</span><span class="sxs-lookup"><span data-stu-id="e9a07-138">Using machine-level discovery simplifies administration of your System Center infrastructure and also allows different versions of the Lync Server management packs (for example, management packs for Lync Server 2010 and management packs for Lync Server 2013) to coexist.</span></span>

<span data-ttu-id="e9a07-139"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9a07-139"></div>

<span> </span>

</div>

</div>

</span></span></div>

