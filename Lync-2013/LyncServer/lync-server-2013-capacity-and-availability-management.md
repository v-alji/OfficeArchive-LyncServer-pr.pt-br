---
title: 'Lync Server 2013: gerenciamento de capacidade e disponibilidade'
description: 'Lync Server 2013: gerenciamento de capacidade e disponibilidade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity and availability management
ms:assetid: 207a2997-f482-4bee-892d-d2b112294481
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720325(v=OCS.15)
ms:contentKeyID: 63969586
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d498649651f8cfbccc65f5b1b5f010025ac418e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435597"
---
# <a name="capacity-and-availability-management-in-lync-server-2013"></a><span data-ttu-id="6921c-103">Gerenciamento de capacidade e disponibilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6921c-103">Capacity and availability management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6921c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6921c-104">

<span> </span></span></span>

<span data-ttu-id="6921c-105">_**Tópico da última modificação:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="6921c-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="6921c-106">A finalidade do gerenciamento de capacidade e gerenciamento de disponibilidade é medir e controlar o desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="6921c-106">The purpose of capacity management and availability management is to measure and control system performance.</span></span> <span data-ttu-id="6921c-107">Recomendamos que você implemente os procedimentos de gerenciamento de capacidade e gerenciamento de disponibilidade para poder medir e controlar o desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="6921c-107">We recommend that you implement capacity management and availability management procedures so that you can measure and control system performance.</span></span> <span data-ttu-id="6921c-108">Você precisa saber se o sistema está disponível e se pode atender às demandas atuais e projetadas definindo linhas de base e monitorando o sistema para procurar tendências.</span><span class="sxs-lookup"><span data-stu-id="6921c-108">You have to know whether the system is available and if it can handle the current and the projected demands by setting baselines and monitoring the system to look for trends.</span></span>

<div>

## <a name="capacity-management"></a><span data-ttu-id="6921c-109">Gerenciamento de capacidade</span><span class="sxs-lookup"><span data-stu-id="6921c-109">Capacity management</span></span>

<span data-ttu-id="6921c-110">O gerenciamento de capacidade envolve o planejamento, o dimensionamento e o controle da capacidade do serviço para ajudar a garantir que os níveis mínimos de desempenho especificados no seu SLA sejam excedidos.</span><span class="sxs-lookup"><span data-stu-id="6921c-110">Capacity management involves planning, sizing, and controlling service capacity to help guarantee that the minimum performance levels specified in your SLA are exceeded.</span></span> <span data-ttu-id="6921c-111">O bom gerenciamento de capacidade ajuda a garantir que você possa fornecer serviços de ti a um custo razoável e ainda atender aos níveis de desempenho definidos em seus SLAs com o cliente.</span><span class="sxs-lookup"><span data-stu-id="6921c-111">Good capacity management helps ensure that you can provide IT services at a reasonable cost and still meet the levels of performance defined in your SLAs with the client.</span></span> <span data-ttu-id="6921c-112">Esses critérios podem incluir o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6921c-112">These criteria can include the following:</span></span>

  - <span data-ttu-id="6921c-113">**Tempo de resposta do sistema**   Esse é o tempo medido que o sistema executa para fazer ações típicas.</span><span class="sxs-lookup"><span data-stu-id="6921c-113">**System Response Time**   This is the measured time that the system takes to do typical actions.</span></span> <span data-ttu-id="6921c-114">Os exemplos incluem o tempo necessário para que a função de servidor de áudio/vídeo processe o tráfego de áudio/vídeo, o tempo necessário para o cliente criar e ingressar em uma conferência, ou o tempo necessário para que a presença seja atualizada em todos os clientes do Inspetor.</span><span class="sxs-lookup"><span data-stu-id="6921c-114">Examples include the time that is required for the audio/video server role to process audio/video traffic, the time that is required for a client to create and join a conference, or the time taken for presence to be updated in all watcher clients.</span></span>

  - <span data-ttu-id="6921c-115">**Capacidade de armazenamento**   Esta é a capacidade de um sistema de armazenamento, seja um banco de dados de conteúdo, um dispositivo de backup ou uma unidade local.</span><span class="sxs-lookup"><span data-stu-id="6921c-115">**Storage Capacity**   This is the capacity of a storage system, whether it is a content database, a backup device, or a local drive.</span></span> <span data-ttu-id="6921c-116">Os exemplos incluem a quantidade máxima de espaço de armazenamento a ser fornecida por site e o momento em que os backups devem ser armazenados antes de serem substituídos.</span><span class="sxs-lookup"><span data-stu-id="6921c-116">Examples include the maximum amount of storage space to be provided per site and the time that backups should be stored before they are overwritten.</span></span>

<span data-ttu-id="6921c-117">Ajustar a capacidade geralmente é um caso de garantir que recursos físicos suficientes estejam disponíveis, como espaço em disco e largura de banda de rede.</span><span class="sxs-lookup"><span data-stu-id="6921c-117">Adjusting capacity is frequently a case of making sure that enough physical resources are available, such as disk space and network bandwidth.</span></span> <span data-ttu-id="6921c-118">A tabela a seguir lista as resoluções típicas de problemas relacionados à capacidade.</span><span class="sxs-lookup"><span data-stu-id="6921c-118">The following table lists typical resolutions for capacity-related issues.</span></span>

### <a name="typical-resolutions-for-capacity-related-issues"></a><span data-ttu-id="6921c-119">Soluções típicas para problemas relacionados à capacidade</span><span class="sxs-lookup"><span data-stu-id="6921c-119">Typical resolutions for capacity-related issues</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6921c-120">Problema</span><span class="sxs-lookup"><span data-stu-id="6921c-120">Issue</span></span></th>
<th><span data-ttu-id="6921c-121">Resolução possível</span><span class="sxs-lookup"><span data-stu-id="6921c-121">Possible resolution</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6921c-122">Usuários remotos com desempenho ruim de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="6921c-122">Remote users having poor audio/video performance</span></span></p></td>
<td><p><span data-ttu-id="6921c-123">Verifique se a largura de banda apropriada está disponível no WAN links e se a QoS está habilitada e devidamente configurada.</span><span class="sxs-lookup"><span data-stu-id="6921c-123">Check to see whether appropriate bandwidth is available on the WAN links and if QoS is enabled and appropriately configured.</span></span> <span data-ttu-id="6921c-124">Verifique os dados de QoE.</span><span class="sxs-lookup"><span data-stu-id="6921c-124">Check QoE data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6921c-125">A resposta geral do ambiente do Lync é lenta.</span><span class="sxs-lookup"><span data-stu-id="6921c-125">Overall response of the Lync environment is slow.</span></span></p></td>
<td><p><span data-ttu-id="6921c-126">Execute testes para verificar se os servidores front-end existentes podem lidar com a carga.</span><span class="sxs-lookup"><span data-stu-id="6921c-126">Run tests to check that the existing front-end servers can deal with the load.</span></span> <span data-ttu-id="6921c-127">Apresente um novo servidor front-end, se necessário. Verifique os tempos de resposta do banco de dados SQL e corrija as causas dos atrasos (por exemplo, melhorar a e/s de disco).</span><span class="sxs-lookup"><span data-stu-id="6921c-127">Introduce a new front-end server if it is needed.Check SQL database response times and fix the causes for the delays (for example, improve disk I/O).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6921c-128">A solução de problemas com mais detalhes é abordada no guia de rede do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6921c-128">Troubleshooting in greater detail is covered in the Lync Server Networking Guide.</span></span>

<span data-ttu-id="6921c-129">A capacidade é afetada pela configuração do sistema e depende de recursos físicos, como largura de banda de rede.</span><span class="sxs-lookup"><span data-stu-id="6921c-129">Capacity is affected by system configuration and depends on physical resources such as network bandwidth.</span></span> <span data-ttu-id="6921c-130">Por exemplo, se um ambiente do Lync estiver configurado para executar um backup completo durante a noite, deve-se tomar cuidado para ajudar a garantir que o efeito sobre o desempenho interativo de usuários finais seja minimizado.</span><span class="sxs-lookup"><span data-stu-id="6921c-130">For example, if a Lync environment is configured to perform a full backup nightly, care must be taken to help guarantee that the effect on the interactive performance experienced by end-users is minimized.</span></span>

<span data-ttu-id="6921c-131">Gerenciamento de capacidade é o processo de manter a capacidade de um sistema dentro dos níveis aceitáveis e soluciona os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="6921c-131">Capacity management is the process of keeping the capacity of a system within acceptable levels and addresses the following issues:</span></span>

  - <span data-ttu-id="6921c-132">**Reagindo a alterações nos requisitos**   Os requisitos de capacidade devem ser ajustados para que as alterações sejam feitas em uma conta do sistema ou da organização.</span><span class="sxs-lookup"><span data-stu-id="6921c-132">**Reacting to changes in requirements**   Capacity requirements have to be adjusted to account for changes in the system or the organization.</span></span> <span data-ttu-id="6921c-133">Por exemplo, se o seu ambiente decidir implementar o Enterprise Voice, o número e o posicionamento dos servidores de mediação e dos gateways da rede de telefonia pública comutada (PSTN) serão muito importantes.</span><span class="sxs-lookup"><span data-stu-id="6921c-133">For example, if your environment decides to implement Enterprise Voice, the number and placement of Mediation Servers and public switched telephone network (PSTN) gateways will be very important.</span></span> <span data-ttu-id="6921c-134">Se você estiver fazendo entroncamento SIP ou Direct SIP, o design geral será alterado de forma significativa para fornecer o melhor desempenho de voz empresarial.</span><span class="sxs-lookup"><span data-stu-id="6921c-134">If you'll be doing Session Initiation Protocol (SIP) trunking or direct SIP, the overall design will be significantly changed to provide the best Enterprise Voice performance.</span></span>

  - <span data-ttu-id="6921c-135">**Prevendo requisitos futuros**   Alguns requisitos de capacidade mudam com previsão ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="6921c-135">**Predicting future requirements**   Some capacity requirements change predictably over time.</span></span> <span data-ttu-id="6921c-136">Rastreando tendências você pode planejar atualizações com antecedência.</span><span class="sxs-lookup"><span data-stu-id="6921c-136">By tracking trends you can plan upgrades in advance.</span></span> <span data-ttu-id="6921c-137">Por exemplo, a largura de banda disponível entre vários sites do Lync deve ser monitorada para criar uma linha de base.</span><span class="sxs-lookup"><span data-stu-id="6921c-137">For example, available bandwidth between various Lync sites must be monitored to create a baseline.</span></span> <span data-ttu-id="6921c-138">Esta linha de base permitirá que você se preveja quando precisa adicionar mais largura de banda a esses links, pois a contagem de usuários nesses sites remotos aumenta com o tempo.</span><span class="sxs-lookup"><span data-stu-id="6921c-138">This baseline will allow you to predict when you have to add more bandwidth to these links as user count in these remote sites increases with time.</span></span>

</div>

<div>

## <a name="availability-management"></a><span data-ttu-id="6921c-139">Gerenciamento de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="6921c-139">Availability management</span></span>

<span data-ttu-id="6921c-140">Gerenciamento de disponibilidade é o processo de garantir que qualquer serviço de ti consistentemente e de forma econômica forneça o nível de serviço confiável, que é necessário para o cliente.</span><span class="sxs-lookup"><span data-stu-id="6921c-140">Availability management is the process of making sure that any IT service consistently and cost effectively delivers the level of consistent, reliable service that is required by the customer.</span></span> <span data-ttu-id="6921c-141">O gerenciamento de disponibilidade lida com a minimização da perda de serviço e com a opção de garantir que a ação adequada seja tomada se o serviço for perdido.</span><span class="sxs-lookup"><span data-stu-id="6921c-141">Availability management deals with minimizing loss of service and with making sure that appropriate action is taken if service is lost.</span></span> <span data-ttu-id="6921c-142">Em um ambiente do Lync, você pode se preocupar em se o serviço Enterprise Voice está disponível, se os usuários podem ingressar em conferências programadas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6921c-142">In a Lync environment, you may be concerned about whether the Enterprise Voice service is available, whether users can join scheduled conferences, and so on.</span></span> <span data-ttu-id="6921c-143">Um SLA define uma frequência e uma duração de paralisação aceitáveis e permite determinados períodos quando o sistema não está disponível para manutenção planejada.</span><span class="sxs-lookup"><span data-stu-id="6921c-143">An SLA defines an acceptable frequency and length of outages and allows for certain periods when the system is unavailable for planned maintenance.</span></span>

<span data-ttu-id="6921c-144">Se você precisar fornecer relatórios ao seu gerenciamento sobre a disponibilidade de sistemas ou se tiver outras penalidades financeiras ou de outras penalidades associadas a destinos de disponibilidade ausentes, deverá gravar dados de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="6921c-144">If you have to provide reports to your management about the availability of systems, or if you have financial or other penalties associated with missing availability targets, you must record availability data.</span></span> <span data-ttu-id="6921c-145">Mesmo que você não tenha esses requisitos formais, é uma boa ideia ao menos saber com que frequência um sistema falhou em um determinado período de tempo.</span><span class="sxs-lookup"><span data-stu-id="6921c-145">Even if you do not have such formal requirements, it is a good idea to at least know how frequently a system has failed in a certain time period.</span></span> <span data-ttu-id="6921c-146">Por exemplo, a disponibilidade do sistema nos últimos 12 meses e o tempo necessário para recuperar-se de cada falha.</span><span class="sxs-lookup"><span data-stu-id="6921c-146">For example, system availability in the last 12 months and how long it took to recover from each failure.</span></span> <span data-ttu-id="6921c-147">Essas informações ajudarão você a medir e melhorar a eficácia da equipe em responder a uma falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="6921c-147">This information will help you measure and improve your team’s effectiveness in responding to a system failure.</span></span> <span data-ttu-id="6921c-148">Ele também pode lhe fornecer informações úteis se houver uma contestação.</span><span class="sxs-lookup"><span data-stu-id="6921c-148">It can also give you useful information if there is a dispute.</span></span>

<span data-ttu-id="6921c-149">As medidas relacionadas à disponibilidade são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="6921c-149">Measures related to availability are as follows:</span></span>

  - <span data-ttu-id="6921c-150">**Disponibilidade**   Isso normalmente é expresso como o tempo que um sistema ou serviço pode ser acessado em comparação com o tempo em que está inoperante.</span><span class="sxs-lookup"><span data-stu-id="6921c-150">**Availability**   This is typically expressed as the time that a system or service can be accessed compared to the time that it is down.</span></span> <span data-ttu-id="6921c-151">Geralmente, é expresso como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="6921c-151">It is typically expressed as a percentage.</span></span> <span data-ttu-id="6921c-152">(Você pode ver referências a "três noves" ou "cinco noves".</span><span class="sxs-lookup"><span data-stu-id="6921c-152">(You may see references to “three nines” or “five nines”.</span></span> <span data-ttu-id="6921c-153">Eles fazem referência a 99,9% ou 99,999% de disponibilidade.)</span><span class="sxs-lookup"><span data-stu-id="6921c-153">These refer to 99.9 percent or 99.999 percent availability.)</span></span>

  - <span data-ttu-id="6921c-154">**Confiabilidade**   Isso é uma medida do tempo entre falhas de um sistema e, às vezes, é expresso como média (ou média) de tempo entre falhas (MTBF).</span><span class="sxs-lookup"><span data-stu-id="6921c-154">**Reliability**   This is a measure of the time between failures of a system and is sometimes expressed as mean (or average) time between failures (MTBF).</span></span>

  - <span data-ttu-id="6921c-155">**Tempo para reparar**   Esse é o tempo levado para recuperar um serviço após uma falha e geralmente é expresso como média (significando a média) tempo para reparar (MTTR).</span><span class="sxs-lookup"><span data-stu-id="6921c-155">**Time to Repair**   This is the time taken to recover a service after a failure has occurred and is often expressed as mean (meaning average) time to repair (MTTR).</span></span>

<span data-ttu-id="6921c-156">A disponibilidade, a confiabilidade e o tempo para reparo estão relacionados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6921c-156">Availability, reliability, and time to repair are related as follows:</span></span>

<span data-ttu-id="6921c-157">**Disponibilidade = (MTBF – MTTR)/MTBF**   Por exemplo, se um servidor falhar duas vezes em um período de seis meses e não estiver disponível para uma média de 20 minutos, o MTBF será de três meses ou 90 dias, e o MTTR será de 20 minutos.</span><span class="sxs-lookup"><span data-stu-id="6921c-157">**Availability = (MTBF – MTTR) / MTBF**   For example, if a server fails two times over a six-month period and is unavailable for an average of 20 minutes, the MTBF is three months or 90 days and the MTTR is 20 minutes.</span></span> <span data-ttu-id="6921c-158">Portanto, Availability = (90 dias – 20 minutos)/90 dias = 99,985%.</span><span class="sxs-lookup"><span data-stu-id="6921c-158">Therefore, Availability = (90 days – 20 minutes) / 90 days = 99.985 percent.</span></span>

<span data-ttu-id="6921c-159">Gerenciamento de disponibilidade é o processo de garantir que a disponibilidade seja maximizada e mantida dentro dos parâmetros definidos em SLAs.</span><span class="sxs-lookup"><span data-stu-id="6921c-159">Availability management is the process of making sure that availability is maximized and kept within the parameters that are defined in SLAs.</span></span> <span data-ttu-id="6921c-160">O gerenciamento de disponibilidade inclui os seguintes processos:</span><span class="sxs-lookup"><span data-stu-id="6921c-160">Availability management includes the following processes:</span></span>

  - <span data-ttu-id="6921c-161">**Monitoramento**    Examinando quando e por quanto tempo os serviços estão indisponíveis.</span><span class="sxs-lookup"><span data-stu-id="6921c-161">**Monitoring**    Examining when and for how long services are unavailable.</span></span>

  - <span data-ttu-id="6921c-162">**Relatório**   Os números de disponibilidade devem ser fornecidos regularmente para gerenciamento, usuários e equipes de operações.</span><span class="sxs-lookup"><span data-stu-id="6921c-162">**Reporting**   Availability figures should be regularly provided to management, users, and operations teams.</span></span> <span data-ttu-id="6921c-163">Esses relatórios devem realçar tendências e identificar áreas bem e áreas que exijam atenção.</span><span class="sxs-lookup"><span data-stu-id="6921c-163">These reports should highlight trends and identify areas that are doing well and areas that require attention.</span></span> <span data-ttu-id="6921c-164">O relatório deve resumir a conformidade com destinos definidos nos SLAs.</span><span class="sxs-lookup"><span data-stu-id="6921c-164">The report should summarize compliance with targets set in the SLAs.</span></span>

  - <span data-ttu-id="6921c-165">**Melhoria**   Se a disponibilidade não atender aos destinos que são definidos nos SLAs ou em que a tendência está na disponibilidade reduzida, o processo de gerenciamento de disponibilidade deve planejar etapas de mídia.</span><span class="sxs-lookup"><span data-stu-id="6921c-165">**Improvement**   If availability does not meet targets that are defined in the SLAs or where the trend is toward reduced availability, the availability management process should plan remedial steps.</span></span> <span data-ttu-id="6921c-166">Isso deve incluir trabalhar com outras equipes responsáveis para realçar os motivos de paralisações e planejar ações corretivas para impedir uma recorrência das paralisações.</span><span class="sxs-lookup"><span data-stu-id="6921c-166">This should include working with other responsible teams to highlight reasons for outages and to plan remedial actions to prevent a recurrence of the outages.</span></span>

<span data-ttu-id="6921c-167">Medidas de capacidade e disponibilidade são tarefas repetitivas que são ideais para ferramentas automatizadas e scripts como o Microsoft System Center Operations Manager (antigo Microsoft Operations Manager), que é abordado mais adiante neste documento.</span><span class="sxs-lookup"><span data-stu-id="6921c-167">Capacity and availability measurements are repetitive tasks that are ideally suited to automated tools and scripts such as Microsoft System Center Operations Manager (formerly Microsoft Operations Manager), which is discussed later in this document.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6921c-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="6921c-168">See Also</span></span>


[<span data-ttu-id="6921c-169">Monitorar o Lync Server 2013 com o System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="6921c-169">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md)  
  

<span data-ttu-id="6921c-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6921c-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

