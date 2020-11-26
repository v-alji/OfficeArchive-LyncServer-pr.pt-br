---
title: 'Lync Server 2013: configuração de integridade no Lync Server'
description: 'Lync Server 2013: configuração de integridade no Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Health configuration in Lync Server 2013
ms:assetid: c00a8c8e-c2d2-4557-8c42-211c7cc96550
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205234(v=OCS.15)
ms:contentKeyID: 48185305
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 999a6d5401cb34382a4120f9255c91c846f72422
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427640"
---
# <a name="health-configuration-in-lync-server-2013"></a><span data-ttu-id="5c569-103">Configuração de integridade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c569-103">Health configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c569-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c569-104">

<span> </span></span></span>

<span data-ttu-id="5c569-105">_**Tópico da última modificação:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="5c569-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="5c569-106">Entre vários sites, artigos da base de dados de conhecimento Microsoft e ferramentas do Lync Server Resource Kit, administradores que encontram problemas ao executar o Lync Server nunca estão longe de uma maneira de solucionar esses problemas.</span><span class="sxs-lookup"><span data-stu-id="5c569-106">Between various websites, Microsoft Knowledge Base articles, and Lync Server Resource Kit tools, administrators who encounter problems when running Lync Server are never far from a way to solve those problems.</span></span>

<span data-ttu-id="5c569-107">Obviamente, não há nenhuma maneira de garantir que você nunca encontrará problemas com o Lync Server 2013 porque o Lync Server pode ser afetado por muitas coisas, como falhas de rede e falhas de hardware, que o próprio produto não pode controlar.</span><span class="sxs-lookup"><span data-stu-id="5c569-107">Obviously there is no way to guarantee that you will never encounter problems with Lync Server 2013 because Lync Server can be affected by many things—like network crashes and hardware failures—that the product itself cannot control.</span></span> <span data-ttu-id="5c569-108">Ao implementar o monitoramento de integridade, os administradores podem identificar possíveis problemas antes que eles se transformem em problemas reais.</span><span class="sxs-lookup"><span data-stu-id="5c569-108">By implementing health monitoring, administrators can identify potential problems before they turn into actual problems.</span></span> <span data-ttu-id="5c569-109">Por exemplo, os administradores podem usar o monitoramento do Lync Server para identificar tendências e tendências.</span><span class="sxs-lookup"><span data-stu-id="5c569-109">For example, administrators can use Lync Server monitoring to identify trends and tendencies.</span></span> <span data-ttu-id="5c569-110">Por exemplo, um aumento constante no número de conferências de áudio/vídeo pode sugerir a necessidade de adicionar capacidade Antes de o sistema ficar sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="5c569-110">For example, a steady increase in the number of audio/video conferences might suggest a need to add capacity before the system becomes overloaded.</span></span>

<span data-ttu-id="5c569-111">De forma semelhante, os administradores podem usar o System Center Operations Manager para fazer coisas como problemas em alertas em tempo real quando ocorrem eventos especificados e para executar transações sintéticas que testem proativamente o sistema.</span><span class="sxs-lookup"><span data-stu-id="5c569-111">In a similar fashion, administrators can use System Center Operations Manager to do such things as issue real-time alerts when specified events occur, and to run synthetic transactions that proactively test the system.</span></span> <span data-ttu-id="5c569-112">As transações sintéticas são usadas no Lync Server para verificar se os usuários podem concluir com êxito tarefas comuns, como fazer logon no sistema, trocar mensagens instantâneas ou fazer chamadas para um telefone localizado na rede telefônica pública comutada (PSTN).</span><span class="sxs-lookup"><span data-stu-id="5c569-112">Synthetic transactions are used in Lync Server to verify that users are able to successfully complete common tasks such as logging on to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="5c569-113">Por exemplo, a execução periódica desses testes pode alertá-lo sobre possíveis problemas com os usuários que fazem logon no Lync Server, além de oferecer a você uma chance de corrigir o problema antes que sua equipe de suporte seja inundada com chamadas de usuários que não conseguem fazer uma conexão.</span><span class="sxs-lookup"><span data-stu-id="5c569-113">For example, periodically running these tests can alert you to potential problems with users logging on to Lync Server, and give you a chance to correct the problem before your support team is flooded with calls from users unable to make a connection.</span></span> <span data-ttu-id="5c569-114">Ao usar o System Center Operations Manager para executar essas transações sintéticas, os administradores podem monitorar rotineiramente a implantação do Lync Server continuamente por 24 horas por dia, sem ter que fazer muitas nada além de responder a qualquer alerta que possa ser emitido.</span><span class="sxs-lookup"><span data-stu-id="5c569-114">By using System Center Operations Manager to run these synthetic transactions, administrators can routinely monitor their deployment of Lync Server continuously for 24 hours every day without having to do much of anything beyond responding to any alerts that might be issued.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5c569-115">Para o Lync Server 2013, o pacote de gerenciamento do System Center Operations Manager também é capaz de detectar problemas "externos" que podem afetar negativamente o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5c569-115">For Lync Server 2013, the Management Pack for System Center Operations Manager is also able to detect "external" issues that can adversely affect Lync Server.</span></span> <span data-ttu-id="5c569-116">Por exemplo, os administradores podem ser notificados se os serviços de informações da Internet (IIS) estiverem offline, os recursos do sistema em um computador do Lync Server ficarão abaixo de um valor especificado ou um computador com o Lync Server sofrer uma falha de hardware.</span><span class="sxs-lookup"><span data-stu-id="5c569-116">For example, administrators can be notified if Internet Information Services (IIS) goes offline, system resources on a Lync Server computer fall below a specified amount, or a Lync Server computer experiences a hardware failure.</span></span>



</div>

<span data-ttu-id="5c569-117">A configuração de integridade no Lync Server 2013 é criada com base no System Center Operations Manager e com o uso de pacotes de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5c569-117">Health configuration in Lync Server 2013 is built around System Center Operations Manager and the use of Lync Server Management Packs.</span></span> <span data-ttu-id="5c569-118">Esses pacotes de gerenciamento incluem vários novos recursos e aprimoramentos, incluindo:</span><span class="sxs-lookup"><span data-stu-id="5c569-118">These Management Packs include a number of new features and enhancements, including:</span></span>

  - <span data-ttu-id="5c569-119">**Disponibilidade do cenário de qualquer local.**</span><span class="sxs-lookup"><span data-stu-id="5c569-119">**Scenario availability from any location.**</span></span> <span data-ttu-id="5c569-120">O pacote de gerenciamento do Lync Server 2010 introduziu o conceito de monitoramento da disponibilidade do cenário do usuário final com transações sintéticas.</span><span class="sxs-lookup"><span data-stu-id="5c569-120">The Lync Server 2010 Management Pack introduced the concept of monitoring end user scenario availability with synthetic transactions.</span></span> <span data-ttu-id="5c569-121">No Lync Server 2013, esses agentes têm transações mais sintéticas e podem ser executados em uma variedade de locais na empresa, de locais geográficos remotos fora da empresa, em filiais do escritório e em implantações do Lync Server 2010 para adicionar cobertura a implantações de bordas legadas.</span><span class="sxs-lookup"><span data-stu-id="5c569-121">In Lync Server 2013, these agents have more synthetic transactions and can be run from a variety of locations inside the enterprise, from remote geographic locations outside of the enterprise, against branch office appliances and against Lync Server 2010 deployments to add coverage to legacy Edge deployments.</span></span>

  - <span data-ttu-id="5c569-122">**Logs de transações sintéticas.**</span><span class="sxs-lookup"><span data-stu-id="5c569-122">**Synthetic transaction logs.**</span></span> <span data-ttu-id="5c569-123">Quando uma transação sintética falha, os administradores têm acesso aos logs HTML para ajudar a determinar o que falhou.</span><span class="sxs-lookup"><span data-stu-id="5c569-123">When a synthetic transaction fails, administrators have access to HTML logs to help determine what failed.</span></span> <span data-ttu-id="5c569-124">Isso inclui compreender qual ação falhou, a latência de cada ação, a linha de comando usada para executar o teste e o erro encontrado.</span><span class="sxs-lookup"><span data-stu-id="5c569-124">This includes understanding which action failed, the latency of each action, the command-line used to run the test, and the error that was encountered.</span></span>

  - <span data-ttu-id="5c569-125">**Maior cobertura de confiabilidade de chamadas.**</span><span class="sxs-lookup"><span data-stu-id="5c569-125">**Increased call reliability coverage.**</span></span> <span data-ttu-id="5c569-126">O pacote de gerenciamento do Lync Server 2010 introduziu alertas de confiabilidade de chamadas para detectar problemas de conectividade graves que afetam as chamadas de áudio de usuários finais.</span><span class="sxs-lookup"><span data-stu-id="5c569-126">The Lync Server 2010 Management Pack introduced call reliability alerting to detect severe connectivity issues that affect the audio calls of end users.</span></span> <span data-ttu-id="5c569-127">Os pacotes de gerenciamento do Lync Server 2013 adicionam cobertura para mensagens instantâneas ponto a ponto (IM) e outros recursos básicos de conferência para maximizar a cobertura e, ao mesmo tempo, reduzir o ruído.</span><span class="sxs-lookup"><span data-stu-id="5c569-127">The Lync Server 2013 Management Packs add coverage for peer-to-peer instant messaging (IM) and other basic conferencing features to maximize coverage while reducing noise.</span></span>

  - <span data-ttu-id="5c569-128">**Monitoramento de dependências.**</span><span class="sxs-lookup"><span data-stu-id="5c569-128">**Dependency monitoring.**</span></span> <span data-ttu-id="5c569-129">Os cenários do Lync Server podem falhar devido a diversos fatores externos, como o IIS offline, recursos de memória e CPU limitados e problemas de disco.</span><span class="sxs-lookup"><span data-stu-id="5c569-129">Lync Server scenarios can fail due to a variety of external factors such as IIS being offline, limited CPU and memory resources, and disk issues.</span></span> <span data-ttu-id="5c569-130">Os novos pacotes de gerenciamento verificam várias dependências críticas para garantir que os administradores tenham conhecimento do impacto.</span><span class="sxs-lookup"><span data-stu-id="5c569-130">The new management packs check several critical dependencies to ensure administrators are aware of their impact.</span></span>

  - <span data-ttu-id="5c569-131">**Relatórios avançados.**</span><span class="sxs-lookup"><span data-stu-id="5c569-131">**Enhanced reporting.**</span></span> <span data-ttu-id="5c569-132">Um conjunto de relatórios para ajudar os administradores a estimar a disponibilidade do cenário, planejar a capacidade e ver quais componentes estão apresentando a maioria dos problemas.</span><span class="sxs-lookup"><span data-stu-id="5c569-132">A set of reports to help administrators estimate scenario availability, plan for capacity, and see which components are experiencing the most issues.</span></span>

<span data-ttu-id="5c569-133">Os pacotes de gerenciamento também incluem uma variedade de recursos para ajudar a detectar e diagnosticar fornecer visibilidade em tempo real para a implantação de integridade do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="5c569-133">The Management Packs also include a variety of features to help detect and diagnose provide real-time visibility into the health your Lync Server deployment.</span></span> <span data-ttu-id="5c569-134">Esses recursos estão listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5c569-134">These features are listed in the following table.</span></span>

### <a name="management-pack-features"></a><span data-ttu-id="5c569-135">Recursos do pacote de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="5c569-135">Management Pack Features</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c569-136">Recurso</span><span class="sxs-lookup"><span data-stu-id="5c569-136">Feature</span></span></th>
<th><span data-ttu-id="5c569-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c569-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c569-138">Transações Sintéticas</span><span class="sxs-lookup"><span data-stu-id="5c569-138">Synthetic Transactions</span></span></p></td>
<td><p><span data-ttu-id="5c569-139">Cmdlets do Windows PowerShell que podem ser executados em diversos locais para garantir que os cenários do usuário final, como entrada, presença, mensagens instantâneas e conferências, estejam prontamente disponíveis para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="5c569-139">Windows PowerShell cmdlets that can be run from various locations to ensure that end user scenarios such as sign-in, presence, IM, and conferencing are readily available to end users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c569-140">Alertas de confiabilidade da chamada</span><span class="sxs-lookup"><span data-stu-id="5c569-140">Call Reliability Alerts</span></span></p></td>
<td><p><span data-ttu-id="5c569-141">Consultas de banco de dados para registros de detalhes de chamadas (CDR).</span><span class="sxs-lookup"><span data-stu-id="5c569-141">Database queries for Call Detail Records (CDR).</span></span> <span data-ttu-id="5c569-142">Esses registros são escritos por servidores front-end para refletir se os usuários finais puderam se conectar a uma chamada ou por que uma chamada foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="5c569-142">These records are written by Front End Servers to reflect whether end users were able to connect to a call or why a call was terminated.</span></span> <span data-ttu-id="5c569-143">Essas consultas resultam em alertas que indicam quando uma ampla variedade de usuários finais está experimentando problemas de conectividade para chamadas ponto a ponto ou funcionalidade básica de conferência.</span><span class="sxs-lookup"><span data-stu-id="5c569-143">These queries result in alerts that indicate when a wide range of end users are experiencing connectivity issues for peer-to-peer calls or basic conferencing functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c569-144">Alertas de qualidade de mídia</span><span class="sxs-lookup"><span data-stu-id="5c569-144">Media Quality Alerts</span></span></p></td>
<td><p><span data-ttu-id="5c569-145">Consultas de banco de dados que procuram relatórios de qualidade da experiência (QoE) publicadas por clientes ao final de cada chamada.</span><span class="sxs-lookup"><span data-stu-id="5c569-145">Database queries that look at Quality of Experience (QoE) reports published by clients at the end of each call.</span></span> <span data-ttu-id="5c569-146">Essas consultas resultam em alertas que apontam cenários em que os usuários podem estar experimentando uma qualidade de mídia ruim durante chamadas e conferências.</span><span class="sxs-lookup"><span data-stu-id="5c569-146">These queries result in alerts that pinpoint scenarios where users are likely to be experiencing poor media quality during calls and conferences.</span></span> <span data-ttu-id="5c569-147">Os dados são criados com base em métricas-chave, como latência e perda de pacotes, que são conhecidos por contribuir diretamente para a qualidade da chamada.</span><span class="sxs-lookup"><span data-stu-id="5c569-147">The data is built upon key metrics such as packet latency and loss, metrics that are known to directly contribute to call quality.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c569-148">Integridade do componente</span><span class="sxs-lookup"><span data-stu-id="5c569-148">Component Health</span></span></p></td>
<td><p><span data-ttu-id="5c569-149">Os componentes individuais do servidor geram alertas usando logs de eventos e contadores de desempenho.</span><span class="sxs-lookup"><span data-stu-id="5c569-149">Individual server components raise alerts by using event logs and performance counters.</span></span> <span data-ttu-id="5c569-150">Esses alertas indicam condições de falha que podem afetar seriamente um ou mais cenários de usuário final.</span><span class="sxs-lookup"><span data-stu-id="5c569-150">These alerts indicate failure conditions that can severely impact one or more end user scenarios.</span></span> <span data-ttu-id="5c569-151">Esses alertas também podem indicar uma variedade de outras condições de falha, incluindo serviços que não estão em execução, altas tarifas de falha, alta latência de mensagem ou problemas de conectividade.</span><span class="sxs-lookup"><span data-stu-id="5c569-151">These alerts can also indicate a variety of other failure conditions, including services not running, high failure rates, high message latency, or connectivity issues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c569-152">Integridade da dependência</span><span class="sxs-lookup"><span data-stu-id="5c569-152">Dependency Health</span></span></p></td>
<td><p><span data-ttu-id="5c569-153">As falhas podem ocorrer por vários motivos externos.</span><span class="sxs-lookup"><span data-stu-id="5c569-153">Failures can occur for a variety of external reasons.</span></span> <span data-ttu-id="5c569-154">Os pacotes de gerenciamento agora monitoram e coletam dados de algumas das principais dependências externas que podem indicar problemas graves, incluindo a disponibilidade do IIS, a CPU e o uso da memória de servidores e processos e métricas de disco.</span><span class="sxs-lookup"><span data-stu-id="5c569-154">The management packs now monitor and collect data for some of the critical external dependencies that might indicate severe issues, including IIS availability, CPU and memory usage of servers and processes, and disk metrics.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5c569-155">Os alertas emitidos pelo sistema foram classificados em três categorias gerais:</span><span class="sxs-lookup"><span data-stu-id="5c569-155">The alerts issued by the system have been classified into three general categories:</span></span>

  - <span data-ttu-id="5c569-156">**Alertas de alta prioridade.**</span><span class="sxs-lookup"><span data-stu-id="5c569-156">**High-priority Alerts.**</span></span> <span data-ttu-id="5c569-157">Esses alertas indicam condições que causarão interrupções de serviço para grupos grandes de usuários.</span><span class="sxs-lookup"><span data-stu-id="5c569-157">These alerts indicate conditions that will cause service outages for large groups of users.</span></span> <span data-ttu-id="5c569-158">Por exemplo, uma falha de componente em uma única máquina não é um alerta de alta prioridade porque o Lync Server 2013 tem recursos de alta disponibilidade internos.</span><span class="sxs-lookup"><span data-stu-id="5c569-158">For example, a component failure on a single machine is not a high-priority alert because Lync Server 2013 has built-in high availability features.</span></span> <span data-ttu-id="5c569-159">Em vez disso, alertas de alta prioridade representam problemas sérios "para ativar os administradores à noite."</span><span class="sxs-lookup"><span data-stu-id="5c569-159">Instead, high-priority alerts represent problems serious enough “to wake up administrators at night.”</span></span> <span data-ttu-id="5c569-160">Paralisações detectadas por transações sintéticas e serviços offline (por exemplo, videoconferência/videoconferência) qualificadas como alertas de alta prioridade.</span><span class="sxs-lookup"><span data-stu-id="5c569-160">Outages detected by synthetic transactions and offline services (for example, audio/video conferencing) qualify as high-priority alerts.</span></span>

  - <span data-ttu-id="5c569-161">**Alertas de prioridade média.**.</span><span class="sxs-lookup"><span data-stu-id="5c569-161">**Medium-priority alerts.**.</span></span> <span data-ttu-id="5c569-162">Esses alertas indicam condições que afetam um subconjunto de usuários ou indicam a degradação da qualidade da chamada.</span><span class="sxs-lookup"><span data-stu-id="5c569-162">These alerts indicate conditions that affect a subset of users or indicate call quality degradation.</span></span> <span data-ttu-id="5c569-163">Isso inclui problemas como falhas de componentes, latência no estabelecimento da chamada ou qualidade de áudio reduzida em chamada.</span><span class="sxs-lookup"><span data-stu-id="5c569-163">That includes problems such as component failures, latency in call establishment, or degraded audio quality in call.</span></span> <span data-ttu-id="5c569-164">Os alertas nessa categoria são stateful e indicam o status atual do problema.</span><span class="sxs-lookup"><span data-stu-id="5c569-164">Alerts in this category are stateful and indicate the current status of the issue.</span></span> <span data-ttu-id="5c569-165">Por exemplo, suponha que seus tempos de estabelecimento de chamadas ultrapassem o limite de alerta.</span><span class="sxs-lookup"><span data-stu-id="5c569-165">For example, suppose your call establishment times exceed the alert threshold.</span></span> <span data-ttu-id="5c569-166">Se o tempo de estabelecimento da chamada retornar ao normal, esses alertas serão resolvidos automaticamente no System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="5c569-166">If call establishment times return to normal, these alerts will be auto-resolved in System Center Operations Manager.</span></span> <span data-ttu-id="5c569-167">A expectativa para esses alertas é que um administrador irá vê-los no mesmo dia útil.</span><span class="sxs-lookup"><span data-stu-id="5c569-167">The expectation for these alerts is that an administrator will look at them on the same business day.</span></span>

  - <span data-ttu-id="5c569-168">**Outros alertas.**</span><span class="sxs-lookup"><span data-stu-id="5c569-168">**Other alerts.**</span></span> <span data-ttu-id="5c569-169">Esses são alertas de componentes que podem afetar um usuário ou subconjunto específico de usuários.</span><span class="sxs-lookup"><span data-stu-id="5c569-169">These are alerts from components that might affect a specific user or subset of users.</span></span> <span data-ttu-id="5c569-170">Por exemplo, talvez o serviço de catálogo de endereços não pudesse analisar a entrada do Active Directory de um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="5c569-170">For example, perhaps the Address Book service could not parse the Active Directory entry of a given user.</span></span> <span data-ttu-id="5c569-171">A expectativa desses alertas é que os administradores os receberão quando tiverem tempo disponível.</span><span class="sxs-lookup"><span data-stu-id="5c569-171">The expectation for these alerts is that administrators will get to them when they have time available.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5c569-172">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5c569-172">In This Section</span></span>

  - [<span data-ttu-id="5c569-173">Configurando o Lync Server 2013 para trabalhar com o System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="5c569-173">Configuring Lync Server 2013 to work with System Center Operations Manager</span></span>](lync-server-2013-configuring-lync-server-to-work-with-system-center-operations-manager.md)

  - [<span data-ttu-id="5c569-174">Usar o log avançado de transações sintéticas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c569-174">Using rich logging for synthetic transactions in Lync Server 2013</span></span>](lync-server-2013-using-rich-logging-for-synthetic-transactions.md)

  - [<span data-ttu-id="5c569-175">Usar o Microsoft SQL Server 2008 R2 como seu banco de dados do System Center Operations Manager para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c569-175">Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database for Lync Server 2013</span></span>](lync-server-2013-using-microsoft-sql-server-2008-r2-as-your-system-center-operations-manager-database.md)

<span data-ttu-id="5c569-176"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c569-176"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

