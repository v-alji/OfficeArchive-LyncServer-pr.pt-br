---
title: 'Lync Server 2013: Posicionamento de dados do Servidor SQL e do arquivo de log'
description: 'Lync Server 2013: dados do SQL Server e posicionamento do arquivo de log.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SQL Server data and log file placement
ms:assetid: 67aa525b-8aa3-474f-827e-8e1d4697f30f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398479(v=OCS.15)
ms:contentKeyID: 48184395
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a127254fec41a734136df9b63fc6cc8929745df7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444592"
---
# <a name="sql-server-data-and-log-file-placement-for-lync-server-2013"></a><span data-ttu-id="b0683-103">Posicionamento de dados do Servidor SQL e do arquivo de log para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0683-103">SQL Server data and log file placement for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0683-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0683-104">

<span> </span></span></span>

<span data-ttu-id="b0683-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="b0683-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="b0683-106">Durante o planejamento e a implantação do Microsoft SQL Server 2012 ou do Microsoft SQL Server 2008 R2 SP1 para seu pool Front-end do Lync Server 2013, uma consideração importante é o posicionamento de dados e arquivos de log em discos rígidos físicos para fins de desempenho.</span><span class="sxs-lookup"><span data-stu-id="b0683-106">During the planning and deployment of Microsoft SQL Server 2012 or Microsoft SQL Server 2008 R2 SP1 for your Lync Server 2013 Front End pool, an important consideration is the placement of data and log files onto physical hard disks for performance.</span></span> <span data-ttu-id="b0683-107">A configuração de disco recomendada é implementar um conjunto de RAID 1 + 0 usando 6 eixos.</span><span class="sxs-lookup"><span data-stu-id="b0683-107">The recommended disk configuration is to implement a 1+0 RAID set using 6 spindles.</span></span> <span data-ttu-id="b0683-108">Colocar todos os arquivos de banco de dados e log que são usados pelo pool de front-end e os serviços e funções de servidor associadas (ou seja, o servidor de arquivamento e monitoramento, o serviço de grupo de resposta do Lync Server, o serviço de estacionamento de chamadas do Lync Server) para o conjunto de drives RAID usando o assistente de implantação do Lync</span><span class="sxs-lookup"><span data-stu-id="b0683-108">Placing all database and log files that are used by the Front End pool and associated server roles and services (that is, Archiving and Monitoring Server, Lync Server Response Group service, Lync Server Call Park service) onto the RAID drive set using the Lync Server Deployment Wizard will result in a configuration that has been tested for good performance.</span></span> <span data-ttu-id="b0683-109">Os arquivos de banco de dados e o que são responsáveis são detalhados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b0683-109">The database files and what they are responsible for is detailed in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b0683-110">Se as suas políticas e configurações do SQL Server exigirem uma instalação mais especializada, os arquivos de banco de dados e de log poderão ser instalados em qualquer local predefinido usando o Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b0683-110">If your policies and SQL Server configurations require a more specialized installation, the database and log files can be installed to any pre-defined location using the Lync Server Management Shell.</span></span> <span data-ttu-id="b0683-111">Consulte <A href="lync-server-2013-database-installation-using-lync-server-management-shell.md">instalação de banco de dados usando o Shell de gerenciamento do Lync Server no Lync server 2013</A> para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="b0683-111">See <A href="lync-server-2013-database-installation-using-lync-server-management-shell.md">Database installation using Lync Server Management Shell in Lync Server 2013</A> for more details.</span></span>



</div>

### <a name="data-and-log-files-for-central-management-store"></a><span data-ttu-id="b0683-112">Arquivos de dados e log para o repositório de gerenciamento central</span><span class="sxs-lookup"><span data-stu-id="b0683-112">Data and Log Files for Central Management Store</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0683-113">Arquivos de banco de dados do repositório de gerenciamento central</span><span class="sxs-lookup"><span data-stu-id="b0683-113">Central Management store database files</span></span></th>
<th><span data-ttu-id="b0683-114">Finalidade de log ou arquivo de dados</span><span class="sxs-lookup"><span data-stu-id="b0683-114">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0683-115">XDS. ldf</span><span class="sxs-lookup"><span data-stu-id="b0683-115">Xds.ldf</span></span></p></td>
<td><p><span data-ttu-id="b0683-116">Arquivo de log de transações para o repositório de gerenciamento central</span><span class="sxs-lookup"><span data-stu-id="b0683-116">Transaction log file for the Central Management store</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0683-117">XDS. MDF</span><span class="sxs-lookup"><span data-stu-id="b0683-117">Xds.mdf</span></span></p></td>
<td><p><span data-ttu-id="b0683-118">Mantém a configuração da topologia atual do Lync Server 2013, conforme definido e publicado pelo construtor de topologias</span><span class="sxs-lookup"><span data-stu-id="b0683-118">Maintains the configuration of the current Lync Server 2013 topology, as defined and published by Topology Builder</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0683-119">Lis. MDF</span><span class="sxs-lookup"><span data-stu-id="b0683-119">Lis.mdf</span></span></p></td>
<td><p><span data-ttu-id="b0683-120">Arquivo de dados do serviço de informações de localização</span><span class="sxs-lookup"><span data-stu-id="b0683-120">Location Information service data file</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0683-121">Lis. ldf</span><span class="sxs-lookup"><span data-stu-id="b0683-121">Lis.ldf</span></span></p></td>
<td><p><span data-ttu-id="b0683-122">Log de transação para o arquivo de dados do local Information Service</span><span class="sxs-lookup"><span data-stu-id="b0683-122">Transaction log for the Location Information service data file</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-user-conferencing-and-address-book"></a><span data-ttu-id="b0683-123">Dados e arquivos de log para o usuário, a conferência e o catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="b0683-123">Data and Log files for User, Conferencing, and Address Book</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0683-124">Principais arquivos de banco de dados do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0683-124">Core Lync Server 2013 database files</span></span></th>
<th><span data-ttu-id="b0683-125">Finalidade de log ou arquivo de dados</span><span class="sxs-lookup"><span data-stu-id="b0683-125">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0683-126">RTC. MDF</span><span class="sxs-lookup"><span data-stu-id="b0683-126">Rtc.mdf</span></span></p></td>
<td><p><span data-ttu-id="b0683-127">Dados persistentes do usuário (por exemplo, listas de controle de acesso (ACLs), contatos, conferências agendadas)</span><span class="sxs-lookup"><span data-stu-id="b0683-127">Persistent user data (for example, access control lists (ACLs), contacts, scheduled conferences)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0683-128">RTC. ldf</span><span class="sxs-lookup"><span data-stu-id="b0683-128">Rtc.ldf</span></span></p></td>
<td><p><span data-ttu-id="b0683-129">Log de transação para dados RTC</span><span class="sxs-lookup"><span data-stu-id="b0683-129">Transaction log for Rtc data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0683-130">RTCDyn. MDF</span><span class="sxs-lookup"><span data-stu-id="b0683-130">Rtcdyn.mdf</span></span></p></td>
<td><p><span data-ttu-id="b0683-131">Mantém dados do usuário transitórios (dados de tempo de execução de presença)</span><span class="sxs-lookup"><span data-stu-id="b0683-131">Maintains transient user data (presence runtime data)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0683-132">RTCDyn. ldf</span><span class="sxs-lookup"><span data-stu-id="b0683-132">Rtcdyn.ldf</span></span></p></td>
<td><p><span data-ttu-id="b0683-133">Log de transação para dados do RTCDyn</span><span class="sxs-lookup"><span data-stu-id="b0683-133">Transaction log for Rtcdyn data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0683-134">RTCAb. MDF</span><span class="sxs-lookup"><span data-stu-id="b0683-134">Rtcab.mdf</span></span></p></td>
<td><p><span data-ttu-id="b0683-135">O banco de dados do catálogo de endereços de comunicação em tempo real (RTC) é o repositório do SQL Server onde as informações do serviço de catálogo de endereços são armazenadas</span><span class="sxs-lookup"><span data-stu-id="b0683-135">Real-time communications (RTC) address book database is the SQL Server repository where Address Book service information is stored</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0683-136">RTCAb. ldf</span><span class="sxs-lookup"><span data-stu-id="b0683-136">Rtcab.ldf</span></span></p></td>
<td><p><span data-ttu-id="b0683-137">Log de transação para o serviço de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="b0683-137">Transaction log for Address Book Service</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0683-138">Rtclocal. mdb</span><span class="sxs-lookup"><span data-stu-id="b0683-138">Rtclocal.mdb</span></span></p></td>
<td><p><span data-ttu-id="b0683-139">Hospeda o diretório de conferências</span><span class="sxs-lookup"><span data-stu-id="b0683-139">Hosts the conference directory</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0683-140">Rtcxds. MDF</span><span class="sxs-lookup"><span data-stu-id="b0683-140">Rtcxds.mdf</span></span></p></td>
<td><p><span data-ttu-id="b0683-141">Mantém o backup dos dados do usuário</span><span class="sxs-lookup"><span data-stu-id="b0683-141">Maintains the backup for user data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0683-142">Rtcxds. ldf</span><span class="sxs-lookup"><span data-stu-id="b0683-142">Rtcxds.ldf</span></span></p></td>
<td><p><span data-ttu-id="b0683-143">Log de transação para dados do Rtcxds</span><span class="sxs-lookup"><span data-stu-id="b0683-143">Transaction log for Rtcxds data</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-call-park-and-response-group"></a><span data-ttu-id="b0683-144">Dados e arquivos de log para estacionamento de chamada e grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="b0683-144">Data and Log Files for Call Park and Response Group</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0683-145">Banco de dados de aplicativos</span><span class="sxs-lookup"><span data-stu-id="b0683-145">Application database</span></span></th>
<th><span data-ttu-id="b0683-146">Finalidade de log ou arquivo de dados</span><span class="sxs-lookup"><span data-stu-id="b0683-146">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0683-147">Cpsdyn. MDF</span><span class="sxs-lookup"><span data-stu-id="b0683-147">Cpsdyn.mdf</span></span></p></td>
<td><p><span data-ttu-id="b0683-148">Banco de dados de informações dinâmicas para o aplicativo parque de chamadas</span><span class="sxs-lookup"><span data-stu-id="b0683-148">Dynamic information database for the Call Park application</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0683-149">Cpsdyn. ldf</span><span class="sxs-lookup"><span data-stu-id="b0683-149">Cpsdyn.ldf</span></span></p></td>
<td><p><span data-ttu-id="b0683-150">Log de transação para o arquivo de dados do aplicativo de estacionamento de chamada</span><span class="sxs-lookup"><span data-stu-id="b0683-150">Transaction log for Call Park application data file</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0683-151">Rgsconfig. MDF</span><span class="sxs-lookup"><span data-stu-id="b0683-151">Rgsconfig.mdf</span></span></p></td>
<td><p><span data-ttu-id="b0683-152">Arquivo de dados do serviço de grupo de resposta do Lync Server para a configuração dos serviços</span><span class="sxs-lookup"><span data-stu-id="b0683-152">Lync Server Response Group service data file for the configuration of the services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0683-153">Rgsconfig. ldf</span><span class="sxs-lookup"><span data-stu-id="b0683-153">Rgsconfig.ldf</span></span></p></td>
<td><p><span data-ttu-id="b0683-154">Arquivo de log de transação para a configuração de aplicativo de grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="b0683-154">Transaction log file for the Response Group application configuration</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0683-155">Rgsdyn. MDF</span><span class="sxs-lookup"><span data-stu-id="b0683-155">Rgsdyn.mdf</span></span></p></td>
<td><p><span data-ttu-id="b0683-156">Arquivo de dados do serviço de grupo de resposta para operações de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="b0683-156">Response Group service data file for runtime operations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0683-157">Rgsdyn. ldf</span><span class="sxs-lookup"><span data-stu-id="b0683-157">Rgsdyn.ldf</span></span></p></td>
<td><p><span data-ttu-id="b0683-158">Log de transação para o arquivo de dados do tempo de execução do serviço de grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="b0683-158">Transaction log for the Response Group service runtime data file</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="data-and-log-files-for-archiving-and-monitoring-server"></a><span data-ttu-id="b0683-159">Arquivos de dados e log para servidor de arquivamento e monitoramento</span><span class="sxs-lookup"><span data-stu-id="b0683-159">Data and Log Files for Archiving and Monitoring Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0683-160">Arquivar e monitorar arquivos de banco de dados</span><span class="sxs-lookup"><span data-stu-id="b0683-160">Archiving and Monitoring database files</span></span></th>
<th><span data-ttu-id="b0683-161">Finalidade de log ou arquivo de dados</span><span class="sxs-lookup"><span data-stu-id="b0683-161">Data file or log purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0683-162">LcsCdr. MDF</span><span class="sxs-lookup"><span data-stu-id="b0683-162">LcsCdr.mdf</span></span></p></td>
<td><p><span data-ttu-id="b0683-163">Repositório de dados para o processo de registro de detalhes de chamadas (CDR) do servidor de monitoramento</span><span class="sxs-lookup"><span data-stu-id="b0683-163">Data store for the call detail recording (CDR) process of the Monitoring Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0683-164">LcsCdr. ldf</span><span class="sxs-lookup"><span data-stu-id="b0683-164">LcsCdr.ldf</span></span></p></td>
<td><p><span data-ttu-id="b0683-165">Log de transação para dados de registro de detalhes de chamadas (CDR)</span><span class="sxs-lookup"><span data-stu-id="b0683-165">Transaction log for call detail recording (CDR) data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0683-166">QoEMetrics. MDF</span><span class="sxs-lookup"><span data-stu-id="b0683-166">QoEMetrics.mdf</span></span></p></td>
<td><p><span data-ttu-id="b0683-167">Arquivo de dados de qualidade da experiência armazenados do servidor de monitoramento</span><span class="sxs-lookup"><span data-stu-id="b0683-167">Quality of Experience data file stored from the Monitoring Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0683-168">QoEMetrics. ldf</span><span class="sxs-lookup"><span data-stu-id="b0683-168">QoEMetrics.ldf</span></span></p></td>
<td><p><span data-ttu-id="b0683-169">Log de transações para monitorar dados</span><span class="sxs-lookup"><span data-stu-id="b0683-169">Transaction log for Monitoring data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0683-170">LcsLog. MDF</span><span class="sxs-lookup"><span data-stu-id="b0683-170">Lcslog.mdf</span></span></p></td>
<td><p><span data-ttu-id="b0683-171">Arquivo de dados para a retenção de mensagens instantâneas e dados de conferência em um servidor de arquivamento</span><span class="sxs-lookup"><span data-stu-id="b0683-171">Data file for the retention of instant messaging and conferencing data on an Archiving Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0683-172">LcsLog. ldf</span><span class="sxs-lookup"><span data-stu-id="b0683-172">Lcslog.ldf</span></span></p></td>
<td><p><span data-ttu-id="b0683-173">Log de transações para arquivar dados</span><span class="sxs-lookup"><span data-stu-id="b0683-173">Transaction log for Archiving data</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b0683-174">Neste tópico, as referências são feitas em disco e em conjunto de RAID.</span><span class="sxs-lookup"><span data-stu-id="b0683-174">In this topic, references are made to disk and to RAID set.</span></span> <span data-ttu-id="b0683-175">Observe que, na configuração de recursos do SQL Server, fazer referência a um disco significa um único dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="b0683-175">Note that in the configuration of SQL Server resources, referring to a disk means a single hardware device.</span></span> <span data-ttu-id="b0683-176">Uma unidade de disco rígido com duas partições, uma contendo arquivos de log e a outra partição que contém os arquivos de dados, não é igual a dois discos, cada um dedicado a arquivos de log ou de dados.</span><span class="sxs-lookup"><span data-stu-id="b0683-176">A hard disk drive with two partitions, one holding log files and the other partition holding data files, is not the same as two disks, each dedicated to either log or data files.</span></span>

<span data-ttu-id="b0683-177">Em referência a conjuntos RAID, há várias tecnologias RAID diferentes de vários fornecedores.</span><span class="sxs-lookup"><span data-stu-id="b0683-177">In reference to RAID sets, there are a number of different RAID technologies from various vendors.</span></span> <span data-ttu-id="b0683-178">E, com a proliferação de redes de área de armazenamento (SAN), os conjuntos de RAID dedicados a um sistema único são mais raros.</span><span class="sxs-lookup"><span data-stu-id="b0683-178">And, with the proliferation of storage area networks (SAN), RAID sets dedicated to a single system are rarer.</span></span> <span data-ttu-id="b0683-179">Você deve consultar seu fornecedor de RAID ou SAN para determinar qual é a melhor configuração para o seu layout de disco ao configurar o desempenho do SQL Server com o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b0683-179">You should consult with your RAID or SAN vendor to determine what the best configuration is for your disk layout when configuring for SQL Server performance with Lync Server 2013.</span></span>

<span data-ttu-id="b0683-180">Observe também que nem todas as unidades de disco são criadas igualmente; alguns têm melhor desempenho do que outros.</span><span class="sxs-lookup"><span data-stu-id="b0683-180">Note also that not all disk drives are created equally; some perform better than others.</span></span> <span data-ttu-id="b0683-181">Mesmo os drives do mesmo fabricante podem variar em desempenho devido à velocidade rotacional, tamanho do cache de hardware e outros fatores.</span><span class="sxs-lookup"><span data-stu-id="b0683-181">Even drives from the same manufacturer can vary in performance because of rotational speed, hardware cache size, and other factors.</span></span>

<span data-ttu-id="b0683-182"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0683-182"></div>

<span> </span>

</div>

</div>

</span></span></div>

