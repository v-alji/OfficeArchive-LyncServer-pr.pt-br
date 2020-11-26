---
title: 'Lync Server 2013: dependências operacionais'
description: 'Lync Server 2013: dependências operacionais.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Operational dependencies
ms:assetid: 450b6be2-7fb3-47d7-8b0b-c05faa331e14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720559(v=OCS.15)
ms:contentKeyID: 63969597
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e240981f5dfded7c27f123c8483794ea3ffedff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445292"
---
# <a name="operational-dependencies-in-lync-server-2013"></a><span data-ttu-id="57cc4-103">Dependências operacionais no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57cc4-103">Operational dependencies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="57cc4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="57cc4-104">

<span> </span></span></span>

<span data-ttu-id="57cc4-105">_**Tópico da última modificação:** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="57cc4-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="57cc4-106">A arquitetura de referência abordada neste documento ajudará a garantir que você tenha uma implantação do Lync Server 2013 que não só pode ser dimensionada para os requisitos da organização, mas é arquitetada de acordo com as práticas recomendadas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="57cc4-106">The Reference Architecture discussed in this document will help ensure that you have a Lync Server 2013 deployment that not only scales to the organization’s requirements but is architected as per Microsoft best practices.</span></span> <span data-ttu-id="57cc4-107">Seja que, como pode ser a implementação do Lync Server 2013 é um serviço dinâmico e como qualquer outro serviço da empresa, ainda exige monitoramento e gerenciamento proativo para manter o alto nível de disponibilidade do serviço e a qualidade do serviço para os negócios.</span><span class="sxs-lookup"><span data-stu-id="57cc4-107">Be that as it may the Lync Server 2013 implementation is a dynamic service and like any other service in the enterprise still requires monitoring and proactive management to maintain high level of service availability and service quality to the business.</span></span>

<span data-ttu-id="57cc4-108">Como o Lync Server 2013 se torna profundamente refinado na empresa diária da organização, é importante que o serviço seja gerenciado pelo gerenciamento de nível de serviço preciso e tangível.</span><span class="sxs-lookup"><span data-stu-id="57cc4-108">As Lync Server 2013 becomes deeply ingrained in the organization’s everyday business it is important that the service be managed by accurate and tangible service level management.</span></span> <span data-ttu-id="57cc4-109">A arquitetura do sistema do Lync pode se tornar complexa e muito integrada e para manter o gerenciamento de nível de serviço efetivo e estabelecer SLAs para o Lync Server 2013 se torna importante compreender as dependências do sistema em outras plataformas e servidores.</span><span class="sxs-lookup"><span data-stu-id="57cc4-109">The Lync system architecture can become complex and very integrated and in order to maintain effective service level management and establish SLAs for Lync Server 2013 it becomes critical to understand the system’s dependencies on other platforms and servers.</span></span> <span data-ttu-id="57cc4-110">Igualmente importante é observar quais serviços comerciais, como aplicativos integrados de voz e UC, se dependem do Lync.</span><span class="sxs-lookup"><span data-stu-id="57cc4-110">Equally important is to note which business services, such as voice and UC integrated applications, become dependent on Lync.</span></span>

<span data-ttu-id="57cc4-111">O Lync Server 2013 deve ser estabelecido anotando todas as dependências mencionadas.</span><span class="sxs-lookup"><span data-stu-id="57cc4-111">Lync Server 2013 must be established noting all the said dependencies.</span></span> <span data-ttu-id="57cc4-112">O mapa de serviços permitirá que você formule um SLA entre o Lync e seu serviço dependente e forneça um local inicial para a negociação de SLA.</span><span class="sxs-lookup"><span data-stu-id="57cc4-112">The service map will allow you to formulate a SLA between Lync and its dependent service and provide a starting place for SLA negotiation.</span></span>

<span data-ttu-id="57cc4-113">A tabela a seguir lista os serviços de dependência típicos para uma infraestrutura do Lync.</span><span class="sxs-lookup"><span data-stu-id="57cc4-113">The following table lists the typical dependency services for a Lync infrastructure.</span></span> <span data-ttu-id="57cc4-114">Cada uma dessas tecnologias deve ter seu próprio monitoramento proativo.</span><span class="sxs-lookup"><span data-stu-id="57cc4-114">Each of these technologies should have its own proactive monitoring.</span></span>

### <a name="typical-dependency-services"></a><span data-ttu-id="57cc4-115">Serviços típicos de dependência</span><span class="sxs-lookup"><span data-stu-id="57cc4-115">Typical dependency services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57cc4-116">Serviço de dependência</span><span class="sxs-lookup"><span data-stu-id="57cc4-116">Dependency Service</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-117">Sistemas operacionais</span><span class="sxs-lookup"><span data-stu-id="57cc4-117">Operating systems</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57cc4-118">Hardware do servidor</span><span class="sxs-lookup"><span data-stu-id="57cc4-118">Server Hardware</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-119">Active Directory</span><span class="sxs-lookup"><span data-stu-id="57cc4-119">Active Directory</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57cc4-120">Infraestrutura de chave pública</span><span class="sxs-lookup"><span data-stu-id="57cc4-120">Public Key Infrastructure</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-121">Serviço de nomes de domínio</span><span class="sxs-lookup"><span data-stu-id="57cc4-121">Domain Naming Service</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57cc4-122">Serviços de banco de dados</span><span class="sxs-lookup"><span data-stu-id="57cc4-122">Database Services</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-123">Serviços de armazenamento</span><span class="sxs-lookup"><span data-stu-id="57cc4-123">Storage Services</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57cc4-124">Gerenciamento de sistema – monitoramento e distribuição</span><span class="sxs-lookup"><span data-stu-id="57cc4-124">System Management – Monitoring and distribution</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-125">Serviços de segurança-antivírus</span><span class="sxs-lookup"><span data-stu-id="57cc4-125">Security Services - Antivirus</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57cc4-126">Infraestrutura de rede-Internet</span><span class="sxs-lookup"><span data-stu-id="57cc4-126">Network Infrastructure - Internet</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-127">Infraestrutura de rede – interna (LAN/WAN)</span><span class="sxs-lookup"><span data-stu-id="57cc4-127">Network Infrastructure – Internal (LAN/WAN)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57cc4-128">Infraestrutura de telefonia – PBX IP e gateways</span><span class="sxs-lookup"><span data-stu-id="57cc4-128">Telephony Infrastructure – IP-PBX and Gateways</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-129">Serviços de nuvem</span><span class="sxs-lookup"><span data-stu-id="57cc4-129">Cloud Services</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="57cc4-130">Pressupõe-se que a organização seja operacionalmente amadureceda em exercer funções básicas de gerenciamento de nível de serviço, como alteração, incidentes e gerenciamento de versão, conforme prescrito pela MOF.</span><span class="sxs-lookup"><span data-stu-id="57cc4-130">It is assumed that the organization is operationally mature in exercising basic service level management functions such as change, incident and release management as prescribed by the MOF.</span></span> <span data-ttu-id="57cc4-131">A solução do Lync deve ser adotada por essas funções e se tornar sujeita aos mesmos processos de gerenciamento operacional.</span><span class="sxs-lookup"><span data-stu-id="57cc4-131">The Lync solution should be adopted by these functions and become subject to the same operational management processes.</span></span>

<span data-ttu-id="57cc4-132">A criação de informações obtidas acima agora tem uma compreensão maior sobre o que pode impactar o serviço do Lync na empresa.</span><span class="sxs-lookup"><span data-stu-id="57cc4-132">Building on the information obtained above we now have a greater understanding of what can impact the Lync service in the enterprise.</span></span> <span data-ttu-id="57cc4-133">Para ajudar a garantir a disponibilidade e a qualidade do serviço do Lync Server 2013, as seguintes ferramentas de monitoramento devem acompanhar a implantação da arquitetura de referência:</span><span class="sxs-lookup"><span data-stu-id="57cc4-133">To help ensure Lync Server 2013 service availability and quality, the following monitoring tools must accompany the reference architecture deployment:</span></span>

### <a name="monitoring-tools"></a><span data-ttu-id="57cc4-134">Ferramentas de monitoramento</span><span class="sxs-lookup"><span data-stu-id="57cc4-134">Monitoring tools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57cc4-135">Componente</span><span class="sxs-lookup"><span data-stu-id="57cc4-135">Component</span></span></th>
<th><span data-ttu-id="57cc4-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="57cc4-136">Description</span></span></th>
<th><span data-ttu-id="57cc4-137">Site aplicável</span><span class="sxs-lookup"><span data-stu-id="57cc4-137">Applicable Site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-138">Lync Server 2013 Monitoring Server</span><span class="sxs-lookup"><span data-stu-id="57cc4-138">Lync Server 2013 Monitoring Server</span></span></p></td>
<td><p><span data-ttu-id="57cc4-139">Implante pelo menos uma função de servidor de monitoramento do Lync Server 2013 por site central e configure o Reporting Pack de qualidade (QoE).</span><span class="sxs-lookup"><span data-stu-id="57cc4-139">Deploy at least one Lync Server 2013 Monitoring Server role per Central site and configure Quality of Experience (QoE) Reporting Pack.</span></span></p>
<p><span data-ttu-id="57cc4-140">Consulte a documentação de implantação do Lync Server 2013 para obter mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="57cc4-140">Refer to the Lync Server 2013 Deployment documentation for further details:</span></span></p>
<p><span data-ttu-id="57cc4-141"><a href="lync-server-2013-deploying-monitoring.md">Implantando o monitoramento no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="57cc4-141"><a href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="57cc4-142">Sites centrais</span><span class="sxs-lookup"><span data-stu-id="57cc4-142">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="57cc4-143">Compartilhamento de cada pool para a sua instância mais próxima da função de servidor de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="57cc4-143">Tether each pool to its nearest instance of the Monitoring Server role.</span></span></p></td>
<td><p><span data-ttu-id="57cc4-144">Sites centrais</span><span class="sxs-lookup"><span data-stu-id="57cc4-144">Central sites</span></span></p>
<p><span data-ttu-id="57cc4-145">Sites de filiais</span><span class="sxs-lookup"><span data-stu-id="57cc4-145">Branch sites</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-146">System Center Operations Manager 2012</span><span class="sxs-lookup"><span data-stu-id="57cc4-146">System Center Operations Manager 2012</span></span></p></td>
<td><p><span data-ttu-id="57cc4-147">System Center Operations Manager 2012 com o pacote de gerenciamento do Microsoft Lync Server 2013 (MP) importado.</span><span class="sxs-lookup"><span data-stu-id="57cc4-147">System Center Operations Manager 2012 with the Microsoft Lync Server 2013 Management Pack (MP) imported.</span></span></p>
<p><span data-ttu-id="57cc4-148">O pacote de gerenciamento implementa a instrumentação baseada em log de eventos e com base em desempenho e contador de desempenho, além de habilitar a instrumentação recém-disponível no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57cc4-148">The Management Pack implements traditional Event Log and Performance counter based instrumentation is utilized as well as enabling newly available instrumentation in Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="57cc4-149">Sites centrais</span><span class="sxs-lookup"><span data-stu-id="57cc4-149">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="57cc4-150">Verifique se a descoberta central para descoberta de funções e componentes que precisam ser monitoradas é automaticamente concluída com base em um script de descoberta central que lê o documento de topologia publicado no banco de dados de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="57cc4-150">Make sure that Central Discovery to discovery of roles and components that need to be monitored are automatically completed based on a central discovery script that reads the topology document published in Central Management Database.</span></span></p></td>
<td><p><span data-ttu-id="57cc4-151">Local central</span><span class="sxs-lookup"><span data-stu-id="57cc4-151">Central Site</span></span></p>
<p><span data-ttu-id="57cc4-152">Site de filial</span><span class="sxs-lookup"><span data-stu-id="57cc4-152">Branch Site</span></span></p>
<p><span data-ttu-id="57cc4-153">Site de borda</span><span class="sxs-lookup"><span data-stu-id="57cc4-153">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="57cc4-154">Implantar agentes do System Centre Operations Manager 2007 em todos os servidores implantados que executam o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="57cc4-154">Deploy System Centre Operations Manager 2007 agents to all deployed servers running Lync Server.</span></span></p></td>
<td><p><span data-ttu-id="57cc4-155">Local central</span><span class="sxs-lookup"><span data-stu-id="57cc4-155">Central Site</span></span></p>
<p><span data-ttu-id="57cc4-156">Site de filial</span><span class="sxs-lookup"><span data-stu-id="57cc4-156">Branch Site</span></span></p>
<p><span data-ttu-id="57cc4-157">Site de borda</span><span class="sxs-lookup"><span data-stu-id="57cc4-157">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="57cc4-158">Certifique-se de que os alertas priorizados estejam configurados para notificação:</span><span class="sxs-lookup"><span data-stu-id="57cc4-158">Make sure Prioritized Alerts are configured for notification:</span></span></p>
<p><span data-ttu-id="57cc4-159">Alertas de alta prioridade</span><span class="sxs-lookup"><span data-stu-id="57cc4-159">High Priority Alerts</span></span></p>
<p><span data-ttu-id="57cc4-160">Alertas de prioridade média</span><span class="sxs-lookup"><span data-stu-id="57cc4-160">Medium Priority Alerts</span></span></p>
<p><span data-ttu-id="57cc4-161">Outros alertas.</span><span class="sxs-lookup"><span data-stu-id="57cc4-161">Other Alerts.</span></span></p></td>
<td><p><span data-ttu-id="57cc4-162">Local central</span><span class="sxs-lookup"><span data-stu-id="57cc4-162">Central Site</span></span></p>
<p><span data-ttu-id="57cc4-163">Site de filial</span><span class="sxs-lookup"><span data-stu-id="57cc4-163">Branch Site</span></span></p>
<p><span data-ttu-id="57cc4-164">Site de borda</span><span class="sxs-lookup"><span data-stu-id="57cc4-164">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="57cc4-165">Configure o monitoramento de porta para a implantação.</span><span class="sxs-lookup"><span data-stu-id="57cc4-165">Configure Port monitoring for your deployment.</span></span></p></td>
<td><p><span data-ttu-id="57cc4-166">Local central</span><span class="sxs-lookup"><span data-stu-id="57cc4-166">Central Site</span></span></p>
<p><span data-ttu-id="57cc4-167">Site de filial</span><span class="sxs-lookup"><span data-stu-id="57cc4-167">Branch Site</span></span></p>
<p><span data-ttu-id="57cc4-168">Site de borda</span><span class="sxs-lookup"><span data-stu-id="57cc4-168">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="57cc4-169">Configurar o monitoramento de URL para a implantação</span><span class="sxs-lookup"><span data-stu-id="57cc4-169">Configure URL monitoring for your deployment</span></span></p></td>
<td><p><span data-ttu-id="57cc4-170">Local central</span><span class="sxs-lookup"><span data-stu-id="57cc4-170">Central Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-171">Integração do Lync e do System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="57cc4-171">Lync and System Center Operations Manager integration</span></span></p></td>
<td><p><span data-ttu-id="57cc4-172">Implantar a confiabilidade das chamadas e a qualidade da mídia MonitoringCall confiabilidade e monitoramento de qualidade da mídia use o computador do Monitoring Server como o nó do inspetor para monitorar a confiabilidade da chamada e a qualidade da mídia do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="57cc4-172">Deploy Call Reliability and Media Quality MonitoringCall reliability and media quality monitoring use the Monitoring Server computer as their watcher node to monitor call reliability and media quality of Lync Server.</span></span> <span data-ttu-id="57cc4-173">Esses dois recursos consultam os bancos de dados do Monitoring Server para fazer a análise.</span><span class="sxs-lookup"><span data-stu-id="57cc4-173">Both of these features query the Monitoring Server databases to do analysis.</span></span></p></td>
<td><p><span data-ttu-id="57cc4-174">Local central</span><span class="sxs-lookup"><span data-stu-id="57cc4-174">Central Site</span></span></p>
<p><span data-ttu-id="57cc4-175">Site de filial</span><span class="sxs-lookup"><span data-stu-id="57cc4-175">Branch Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="57cc4-176">Verifique se os limites de aviso de qualidade de mídia estão configurados com precisão.</span><span class="sxs-lookup"><span data-stu-id="57cc4-176">Ensure Media Quality warning thresholds are accurately configured.</span></span> <span data-ttu-id="57cc4-177">A tabela a seguir indica a pontuação máxima média de opinião da rede por codec.</span><span class="sxs-lookup"><span data-stu-id="57cc4-177">The following table indicates the maximum Network Mean Opinion Scores by Codec.</span></span> <span data-ttu-id="57cc4-178">Em produção, essas classificações devem ser monitoradas por um período definido e os limites aceitáveis devem ser estabelecidos com base nas pontuações específicas do NMOS da organização.</span><span class="sxs-lookup"><span data-stu-id="57cc4-178">In production these scores should be monitored for a set period and acceptable thresholds must be established based on the organization specific NMOS scores.</span></span></p></td>
<td><p><span data-ttu-id="57cc4-179">Local central</span><span class="sxs-lookup"><span data-stu-id="57cc4-179">Central Site</span></span></p>
<p><span data-ttu-id="57cc4-180">Site de filial</span><span class="sxs-lookup"><span data-stu-id="57cc4-180">Branch Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-181">Inspetor de transação sintética do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57cc4-181">Lync Server 2013 Synthetic Transaction Watcher</span></span></p></td>
<td><p><span data-ttu-id="57cc4-182">Implantar um Lync Server dedicado para ser um inspetor de transação sintética.</span><span class="sxs-lookup"><span data-stu-id="57cc4-182">Deploy a dedicated Lync Server to be a synthetic transaction watcher.</span></span></p>
<p><span data-ttu-id="57cc4-183">As transações sintéticas são cmdlets do Windows PowerShell do Lync Server 2013 que são automaticamente disparados pelo pacote de gerenciamento em um intervalo predefinido.</span><span class="sxs-lookup"><span data-stu-id="57cc4-183">Synthetic transactions are Lync Server 2013 Windows PowerShell cmdlets that are automatically triggered by the management pack on a predefined interval.</span></span> <span data-ttu-id="57cc4-184">Eles são executados em um nó de Inspetor de transação sintética que é um servidor designado pelo administrador responsável pela descoberta e execução do STs para cada pool.</span><span class="sxs-lookup"><span data-stu-id="57cc4-184">These are executed on a synthetic transaction watcher node which is an administrator designated server responsible for discovery and execution of STs for each pool.</span></span></p>
<p><span data-ttu-id="57cc4-185">Não recomendamos que você use um servidor Microsoft Lync Server 2013 existente como um nó Inspetor de transação sintética.</span><span class="sxs-lookup"><span data-stu-id="57cc4-185">We do not recommend that you use an existing Microsoft Lync Server 2013 server as a synthetic transaction watcher node.</span></span> <span data-ttu-id="57cc4-186">Isso se deve a altos requisitos de uso de CPU/memória para executar o STs.</span><span class="sxs-lookup"><span data-stu-id="57cc4-186">This is due to the high CPU/memory usage requirements for running STs.</span></span> <span data-ttu-id="57cc4-187">Use um novo computador servidor (ou um servidor virtual) para o nó Inspetor de transação sintética.</span><span class="sxs-lookup"><span data-stu-id="57cc4-187">Use a new server computer (or a virtual server) for the synthetic transaction watcher node.</span></span></p></td>
<td><p><span data-ttu-id="57cc4-188">Local central</span><span class="sxs-lookup"><span data-stu-id="57cc4-188">Central Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="57cc4-189">Implantando o nó Inspetor de transações sintéticas.</span><span class="sxs-lookup"><span data-stu-id="57cc4-189">Deploying synthetic transactions watcher node.</span></span></p>
<p><span data-ttu-id="57cc4-190">Consulte o documento MonitoringCS_withSCOM.docx da documentação do UCTAP Connect.</span><span class="sxs-lookup"><span data-stu-id="57cc4-190">Refer to the MonitoringCS_withSCOM.docx document from UCTAP connect documentation.</span></span></p></td>
<td><p><span data-ttu-id="57cc4-191">Local central</span><span class="sxs-lookup"><span data-stu-id="57cc4-191">Central Site</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="maximum-network-mos-scores-per-codec"></a><span data-ttu-id="57cc4-192">Máximo de pontuações de rede MOS por codec</span><span class="sxs-lookup"><span data-stu-id="57cc4-192">Maximum Network MOS scores per codec</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57cc4-193">Cenário</span><span class="sxs-lookup"><span data-stu-id="57cc4-193">Scenario</span></span></th>
<th><span data-ttu-id="57cc4-194">Codec</span><span class="sxs-lookup"><span data-stu-id="57cc4-194">Codec</span></span></th>
<th><span data-ttu-id="57cc4-195">NMOS máx.</span><span class="sxs-lookup"><span data-stu-id="57cc4-195">Max NMOS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-196">UC – chamada UC</span><span class="sxs-lookup"><span data-stu-id="57cc4-196">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="57cc4-197">RTAudio WB</span><span class="sxs-lookup"><span data-stu-id="57cc4-197">RTAudio WB</span></span></p></td>
<td><p><span data-ttu-id="57cc4-198">4,10</span><span class="sxs-lookup"><span data-stu-id="57cc4-198">4.10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57cc4-199">UC – chamada UC</span><span class="sxs-lookup"><span data-stu-id="57cc4-199">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="57cc4-200">RTAudio NB</span><span class="sxs-lookup"><span data-stu-id="57cc4-200">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="57cc4-201">2,95</span><span class="sxs-lookup"><span data-stu-id="57cc4-201">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-202">Chamada de conferência</span><span class="sxs-lookup"><span data-stu-id="57cc4-202">Conference call</span></span></p></td>
<td><p><span data-ttu-id="57cc4-203">Siren</span><span class="sxs-lookup"><span data-stu-id="57cc4-203">Siren</span></span></p></td>
<td><p><span data-ttu-id="57cc4-204">3,72</span><span class="sxs-lookup"><span data-stu-id="57cc4-204">3.72</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57cc4-205">UC – chamada PSTN</span><span class="sxs-lookup"><span data-stu-id="57cc4-205">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="57cc4-206">RTAudio NB</span><span class="sxs-lookup"><span data-stu-id="57cc4-206">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="57cc4-207">2,95</span><span class="sxs-lookup"><span data-stu-id="57cc4-207">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57cc4-208">UC – chamada PSTN</span><span class="sxs-lookup"><span data-stu-id="57cc4-208">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="57cc4-209">G-711</span><span class="sxs-lookup"><span data-stu-id="57cc4-209">G-711</span></span></p></td>
<td><p><span data-ttu-id="57cc4-210">3,61</span><span class="sxs-lookup"><span data-stu-id="57cc4-210">3.61</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="57cc4-211">Acima e acima das atividades anteriores de monitoramento do Pro-active, as tarefas de manutenção devem ser executadas para sites centrais, de periféricos e de filiais com base diária, semanal e mensal, conforme definido no guia de operações de RA do Lync.</span><span class="sxs-lookup"><span data-stu-id="57cc4-211">Over and above the previous pro-active monitoring activities, maintenance tasks should be executed for Central, Edge and Branch sites on a recurring daily, weekly and monthly basis as defined in the Lync RA Operations Guide.</span></span>

<span data-ttu-id="57cc4-212"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="57cc4-212"></div>

<span> </span>

</div>

</div>

</span></span></div>

