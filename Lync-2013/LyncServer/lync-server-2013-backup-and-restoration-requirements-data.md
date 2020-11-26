---
title: 'Lync Server 2013: requisitos de backup e restauração: dados'
description: 'Lync Server 2013: requisitos de backup e restauração: dados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Backup and restoration requirements: data'
ms:assetid: ecfb8e4d-cb4f-476d-9772-4486bd683c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202194(v=OCS.15)
ms:contentKeyID: 51541526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7e135f09706d31ff3f0efa54c8687546de9fab78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437984"
---
# <a name="backup-and-restoration-requirements-in-lync-server-2013-data"></a><span data-ttu-id="fe07e-103">Requisitos de backup e restauração no Lync Server 2013: dados</span><span class="sxs-lookup"><span data-stu-id="fe07e-103">Backup and restoration requirements in Lync Server 2013: data</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fe07e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fe07e-104">

<span> </span></span></span>

<span data-ttu-id="fe07e-105">_**Tópico da última modificação:** 2013-03-26_</span><span class="sxs-lookup"><span data-stu-id="fe07e-105">_**Topic Last Modified:** 2013-03-26_</span></span>

<span data-ttu-id="fe07e-106">O Lync Server usa configurações e informações de configuração que são armazenadas em bancos de dados e dados armazenados em bancos de dados e repositórios de arquivos.</span><span class="sxs-lookup"><span data-stu-id="fe07e-106">Lync Server uses settings and configuration information that are stored in databases, and data that is stored in databases and file stores.</span></span> <span data-ttu-id="fe07e-107">Este tópico descreve os dados dos quais você precisa fazer backup para restaurar o serviço se a sua organização tiver uma falha ou uma interrupção, além de identificar os dados e os componentes usados pelo Lync Server dos quais você precisa fazer backup separadamente.</span><span class="sxs-lookup"><span data-stu-id="fe07e-107">This topic describes the data that you need to back up to be able to restore service if your organization experiences a failure or outage, and also identifies the data and components used by Lync Server that you need to back up separately.</span></span>

<div>

## <a name="settings-and-configuration-requirements"></a><span data-ttu-id="fe07e-108">Configurações e requisitos de configuração</span><span class="sxs-lookup"><span data-stu-id="fe07e-108">Settings and Configuration Requirements</span></span>

<span data-ttu-id="fe07e-109">Este tópico inclui procedimentos para fazer o backup e a restauração das configurações e informações de configuração necessárias para a recuperação do serviço do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe07e-109">This topic includes procedures for backing up and restoring the settings and configuration information that is required for recovery of Lync Server service.</span></span> <span data-ttu-id="fe07e-110">As informações de configuração estão localizadas no repositório de gerenciamento central ou em outro banco de dados back-end ou no servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="fe07e-110">The configuration information is located in the Central Management store or on another back-end database or on Standard Edition server.</span></span>

<span data-ttu-id="fe07e-111">A tabela a seguir identifica as configurações e informações de configuração das quais você precisa fazer backup e restaurar.</span><span class="sxs-lookup"><span data-stu-id="fe07e-111">The following table identifies the settings and configuration information that you need to back up and restore.</span></span>

### <a name="settings-and-configuration-data"></a><span data-ttu-id="fe07e-112">Configurações e dados de configuração</span><span class="sxs-lookup"><span data-stu-id="fe07e-112">Settings and Configuration Data</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe07e-113">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fe07e-113">Type of data</span></span></th>
<th><span data-ttu-id="fe07e-114">Onde armazenado</span><span class="sxs-lookup"><span data-stu-id="fe07e-114">Where stored</span></span></th>
<th><span data-ttu-id="fe07e-115">Descrição/quando fazer backup</span><span class="sxs-lookup"><span data-stu-id="fe07e-115">Description / When to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe07e-116">Informações de configuração de topologia</span><span class="sxs-lookup"><span data-stu-id="fe07e-116">Topology configuration information</span></span></p></td>
<td><p><span data-ttu-id="fe07e-117">Repositório de gerenciamento central (banco de dados: XDS. MDF)</span><span class="sxs-lookup"><span data-stu-id="fe07e-117">Central Management store (database: Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="fe07e-118">Configurações de topologia, política e configuração.</span><span class="sxs-lookup"><span data-stu-id="fe07e-118">Topology, policy, and configuration settings.</span></span></p>
<p><span data-ttu-id="fe07e-119">Faça backup com seus backups regulares e depois de usar os cmdlets ou o painel de controle do Lync Server para modificar sua configuração ou políticas.</span><span class="sxs-lookup"><span data-stu-id="fe07e-119">Back up with your regular backups and after you use Lync Server Control Panel or cmdlets to modify your configuration or policies.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe07e-120">Informações de localização</span><span class="sxs-lookup"><span data-stu-id="fe07e-120">Location information</span></span></p></td>
<td><p><span data-ttu-id="fe07e-121">Repositório de gerenciamento central (banco de dados: Lis. MDF)</span><span class="sxs-lookup"><span data-stu-id="fe07e-121">Central Management store (database: Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="fe07e-122">Informações de configuração do 9-1-1 (E9-1-1) avançada do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="fe07e-122">Enterprise Voice Enhanced 9-1-1 (E9-1-1) configuration information.</span></span> <span data-ttu-id="fe07e-123">Geralmente, essas informações são estáticas.</span><span class="sxs-lookup"><span data-stu-id="fe07e-123">This information is generally static.</span></span></p>
<p><span data-ttu-id="fe07e-124">Faça backup com seus backups regulares.</span><span class="sxs-lookup"><span data-stu-id="fe07e-124">Back up with your regular backups.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe07e-125">Informações de configuração do grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="fe07e-125">Response Group configuration information</span></span></p></td>
<td><p><span data-ttu-id="fe07e-126">Servidor back-end ou servidor Standard Edition (banco de dados: RgsConfig. MDF)</span><span class="sxs-lookup"><span data-stu-id="fe07e-126">Back End Server or Standard Edition server (database: RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="fe07e-127">Grupo de resposta grupos, filas e fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fe07e-127">Response Group agent groups, queues, and workflows.</span></span></p>
<p><span data-ttu-id="fe07e-128">Faça backup com seus backups regulares e depois de adicionar ou alterar grupos de agente, filas ou fluxos de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fe07e-128">Back up with your regular backups and after you add or change agent groups, queues, or workflows.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="data-requirements"></a><span data-ttu-id="fe07e-129">Requisitos de dados</span><span class="sxs-lookup"><span data-stu-id="fe07e-129">Data Requirements</span></span>

<span data-ttu-id="fe07e-130">Aqui está uma lista dos dados do Lync Server dos quais você precisa fazer backup para que você possa restaurar o serviço do Lync Server em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="fe07e-130">Here is a list of the Lync Server data that you need to back up so that you can restore Lync Server service in the event of a failure.</span></span>

<span data-ttu-id="fe07e-131">Observe que alguns tipos de dados não são necessários para a recuperação.</span><span class="sxs-lookup"><span data-stu-id="fe07e-131">Note that some types of data are not required for recovery.</span></span> <span data-ttu-id="fe07e-132">Este tópico não contém procedimentos para fazer backup desses tipos de dados, que incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fe07e-132">This topic does not contain procedures for backing up these types of data, which include the following:</span></span>

  - <span data-ttu-id="fe07e-133">Dados de usuários transitórios, como pontos de extremidade e assinaturas, servidores de conferência ativos e Estados de conferência transitória (banco de dados: RtcDyn. MDF)</span><span class="sxs-lookup"><span data-stu-id="fe07e-133">Transient user data, such as endpoints and subscriptions, active conferencing servers, and transient conferencing states (database: RtcDyn.mdf)</span></span>

  - <span data-ttu-id="fe07e-134">Dados de catálogo de endereços (bancos de dados: RTCAb. MDF e Rtcab1. MDF).</span><span class="sxs-lookup"><span data-stu-id="fe07e-134">Address Book data (databases: Rtcab.mdf and Rtcab1.mdf).</span></span> <span data-ttu-id="fe07e-135">O banco de dados do catálogo de endereços é regenerado automaticamente dos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fe07e-135">The Address Book database is regenerated automatically from Active Directory Domain Services.</span></span>

  - <span data-ttu-id="fe07e-136">Informações dinâmicas para o aplicativo parque de chamadas (banco de dados: CpsDyn. MDF)</span><span class="sxs-lookup"><span data-stu-id="fe07e-136">Dynamic information for the Call Park application (database: CpsDyn.mdf)</span></span>

  - <span data-ttu-id="fe07e-137">Dados de grupo de resposta transitório, como estado de entrada do agente e informações de chamada em espera (banco de dados: RgsDyn. MDF)</span><span class="sxs-lookup"><span data-stu-id="fe07e-137">Transient Response Group data, such as agent sign-in state and call waiting information (database: RgsDyn.mdf)</span></span>

  - <span data-ttu-id="fe07e-138">O banco de dados de conformidade para chats persistentes (banco de dados: MgcComp. MDF).</span><span class="sxs-lookup"><span data-stu-id="fe07e-138">The compliance database for Persistent Chat (database: MgcComp.mdf).</span></span> <span data-ttu-id="fe07e-139">Se a conformidade de chat persistente estiver habilitada, as informações no banco de dados de conformidade de chat persistente serão transitórias desde que você tenha um adaptador configurado para ler as informações do banco de dados e convertê-las em um formato alternativo.</span><span class="sxs-lookup"><span data-stu-id="fe07e-139">If you have Persistent Chat compliance enabled, the information in the Persistent Chat Compliance database is transient as long as you have an adapter configured to read information from the database and convert it to an alternate format.</span></span> <span data-ttu-id="fe07e-140">Portanto, o banco de dados de conformidade para chats persistentes é considerado transitório.</span><span class="sxs-lookup"><span data-stu-id="fe07e-140">Hence the compliance database for Persistent Chat is considered transient.</span></span>
    
    <span data-ttu-id="fe07e-141">O servidor de chat persistente do Lync Server 2013 vem com um adaptador XML.</span><span class="sxs-lookup"><span data-stu-id="fe07e-141">Lync Server 2013 Persistent Chat Server ships with an XML adapter.</span></span> <span data-ttu-id="fe07e-142">Você também pode instalar adaptadores personalizados que tomam esses dados e movê-los para outras fontes, como arquivos Exchange hospedados.</span><span class="sxs-lookup"><span data-stu-id="fe07e-142">You can also install custom adapters that take this data and move it to other sources, such as Exchange Hosted Archives.</span></span>

<span data-ttu-id="fe07e-143">A tabela a seguir identifica os dados dos quais você precisa fazer backup e restaurar.</span><span class="sxs-lookup"><span data-stu-id="fe07e-143">The following table identifies the data that you need to back up and restore.</span></span>

### <a name="data-stored-in-databases"></a><span data-ttu-id="fe07e-144">Dados armazenados em bancos de dados</span><span class="sxs-lookup"><span data-stu-id="fe07e-144">Data Stored in Databases</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe07e-145">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fe07e-145">Type of data</span></span></th>
<th><span data-ttu-id="fe07e-146">Onde armazenado</span><span class="sxs-lookup"><span data-stu-id="fe07e-146">Where stored</span></span></th>
<th><span data-ttu-id="fe07e-147">Descrição/quando fazer backup</span><span class="sxs-lookup"><span data-stu-id="fe07e-147">Description / When to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe07e-148">Dados persistentes do usuário</span><span class="sxs-lookup"><span data-stu-id="fe07e-148">Persistent user data</span></span></p></td>
<td><p><span data-ttu-id="fe07e-149">Servidor back-end ou servidor Standard Edition (banco de dados: RTCXDS. MDF)</span><span class="sxs-lookup"><span data-stu-id="fe07e-149">Back End Server or Standard Edition server (database: RTCXDS.mdf)</span></span></p></td>
<td><p><span data-ttu-id="fe07e-150">Direitos de usuário, listas de contatos do usuário, dados de servidor ou pool, conferências programadas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="fe07e-150">User rights, user Contacts lists, server or pool data, scheduled conferences, and so on.</span></span> <span data-ttu-id="fe07e-151">Estes dados do usuário não incluem o conteúdo carregado em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="fe07e-151">This user data does not include content uploaded to a conference.</span></span></p>
<p><span data-ttu-id="fe07e-152">Faça backup com seus backups regulares.</span><span class="sxs-lookup"><span data-stu-id="fe07e-152">Back up with your regular backups.</span></span> <span data-ttu-id="fe07e-153">Essas informações são dinâmicas, mas a perda de atualizações não é catastrófica no Lync Server, caso seja necessário restaurar o último backup regular.</span><span class="sxs-lookup"><span data-stu-id="fe07e-153">This information is dynamic, but the loss of updates is not catastrophic to Lync Server if you need to restore to your last regular backup.</span></span> <span data-ttu-id="fe07e-154">Se as listas de contatos forem essenciais para a sua organização, você poderá fazer backup desses dados com mais frequência.</span><span class="sxs-lookup"><span data-stu-id="fe07e-154">If Contacts lists are critical to your organization, you can back up this data more frequently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe07e-155">Arquivar dados</span><span class="sxs-lookup"><span data-stu-id="fe07e-155">Archiving data</span></span></p></td>
<td><p><span data-ttu-id="fe07e-156">Banco de dados de arquivamento (banco de dados: LcsLog. MDF)</span><span class="sxs-lookup"><span data-stu-id="fe07e-156">Archiving database (database: LcsLog.mdf)</span></span></p>
<p><span data-ttu-id="fe07e-157">Esses dados podem ser armazenados no Exchange 2013, se você tiver habilitado a opção de integração do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe07e-157">This data may be stored on Exchange 2013, if you have enabled the Microsoft Exchange integration option.</span></span> <span data-ttu-id="fe07e-158">Caso contrário, esses dados são mantidos em um banco de dados de arquivamento do Lync Server, que pode ser posicionado com outro banco de dados do Lync Server ou autônomo em um servidor de banco de dados separado.</span><span class="sxs-lookup"><span data-stu-id="fe07e-158">Otherwise, this data is kept in a Lync Server Archiving database, which may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="fe07e-159">Mensagens instantâneas (IM) e conteúdo da reunião.</span><span class="sxs-lookup"><span data-stu-id="fe07e-159">Instant messaging (IM) and meeting content.</span></span></p>
<p><span data-ttu-id="fe07e-160">Esses dados não são críticos para o Lync Server, mas podem ser críticos para a sua organização para fins reguladores.</span><span class="sxs-lookup"><span data-stu-id="fe07e-160">This data is not critical to Lync Server, but it may be critical to your organization for regulatory purposes.</span></span> <span data-ttu-id="fe07e-161">Determine o seu cronograma de backup de acordo.</span><span class="sxs-lookup"><span data-stu-id="fe07e-161">Determine your back up schedule accordingly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe07e-162">Monitorando dados</span><span class="sxs-lookup"><span data-stu-id="fe07e-162">Monitoring data</span></span></p></td>
<td><p><span data-ttu-id="fe07e-163">Bancos de dados de monitoramento (LcsCDR. MDF e QoeMetrics. MDF)</span><span class="sxs-lookup"><span data-stu-id="fe07e-163">Monitoring databases (LcsCDR.mdf and QoeMetrics.mdf)</span></span></p>
<p><span data-ttu-id="fe07e-164">Esses bancos de dados podem estar posicionados com outro banco de dados do Lync Server ou autônomo em um servidor de banco de dados separado.</span><span class="sxs-lookup"><span data-stu-id="fe07e-164">These databases may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="fe07e-165">Registros de detalhes da chamada (LcsCDR. MDF) e métricas de qualidade da experiência (QoE) (QoeMetrics. MDF).</span><span class="sxs-lookup"><span data-stu-id="fe07e-165">Call detail records (LcsCDR.mdf) and Quality of Experience (QoE) metrics (QoeMetrics.mdf).</span></span></p>
<p><span data-ttu-id="fe07e-166">Os registros de detalhes da chamada são dinâmicos e podem ser críticos para a sua empresa.</span><span class="sxs-lookup"><span data-stu-id="fe07e-166">Call detail records are dynamic and may be critical to your business.</span></span> <span data-ttu-id="fe07e-167">Determine o seu cronograma de backup, considerando se você precisa desses registros por motivos reguladores.</span><span class="sxs-lookup"><span data-stu-id="fe07e-167">Determine your back up schedule by considering whether you need these records for regulatory reasons.</span></span></p>
<p><span data-ttu-id="fe07e-168">As informações de qualidade da experiência são dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="fe07e-168">Quality of experience information is dynamic.</span></span> <span data-ttu-id="fe07e-169">A perda de dados de QoE não é essencial para a operação do Lync Server, mas pode ser fundamental para a sua empresa.</span><span class="sxs-lookup"><span data-stu-id="fe07e-169">Loss of QoE data is not critical for the operation of Lync Server, but it may be critical to your business.</span></span> <span data-ttu-id="fe07e-170">Determine sua agenda de backup com base em quão críticas essas informações são para sua organização.</span><span class="sxs-lookup"><span data-stu-id="fe07e-170">Determine your back up schedule based on how critical this information is to your organization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe07e-171">Dados de chat persistente</span><span class="sxs-lookup"><span data-stu-id="fe07e-171">Persistent Chat data</span></span></p></td>
<td><p><span data-ttu-id="fe07e-172">Banco de dados de chat persistente (MGD. MDF).</span><span class="sxs-lookup"><span data-stu-id="fe07e-172">Persistent Chat database (mgd.mdf).</span></span></p>
<p><span data-ttu-id="fe07e-173">Esse banco de dados pode estar posicionado com outro banco de dados do Lync Server ou autônomo em um servidor de banco de dados separado.</span><span class="sxs-lookup"><span data-stu-id="fe07e-173">This database may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="fe07e-174">Dados de chat persistentes são postados pelo conteúdo real do chat em salas de chat.</span><span class="sxs-lookup"><span data-stu-id="fe07e-174">Persistent Chat Data is actual chat content being posted in chat rooms.</span></span> <span data-ttu-id="fe07e-175">Geralmente, esses dados são críticos para os negócios.</span><span class="sxs-lookup"><span data-stu-id="fe07e-175">This data is often business critical.</span></span></p>
<p><span data-ttu-id="fe07e-176">Você pode optar por usar o backup do SQL Server ou exportar o banco de dados usando o cmdlet <strong>Export-CsPersistentChatData</strong> fornecido no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe07e-176">You can choose to use SQL Server backup, or export the database by using the <strong>Export-CsPersistentChatData</strong> cmdlet that is provided in Lync Server.</span></span> <span data-ttu-id="fe07e-177">Para a recuperação dos dados, você pode importar e restaurar o banco de dados para o ponto do último backup completo, o que significa que você não pode restaurar o banco de dados ao ponto de falha.</span><span class="sxs-lookup"><span data-stu-id="fe07e-177">For recovery of the data, you can import and restore the database to the point of the last full backup, which means you cannot restore the database to the point of failure.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="file-store-data-requirements"></a><span data-ttu-id="fe07e-178">Requisitos de dados do repositório de arquivos</span><span class="sxs-lookup"><span data-stu-id="fe07e-178">File Store Data Requirements</span></span>

<span data-ttu-id="fe07e-179">Em uma implantação do Enterprise Edition, o armazenamento de arquivos do Lync Server geralmente está localizado em um servidor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="fe07e-179">In an Enterprise Edition deployment, the Lync Server file store is typically located on a file server.</span></span> <span data-ttu-id="fe07e-180">Em uma implantação de edição padrão, o repositório de arquivos do Lync Server está localizado por padrão no servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="fe07e-180">In a Standard Edition deployment, the Lync Server file store is located by default on the Standard Edition server.</span></span> <span data-ttu-id="fe07e-181">Geralmente, há um repositório de arquivos do Lync Server que é compartilhado para um site.</span><span class="sxs-lookup"><span data-stu-id="fe07e-181">Typically, there is one Lync Server file store that is shared for a site.</span></span> <span data-ttu-id="fe07e-182">O repositório de arquivos de chat persistente usa o mesmo compartilhamento de arquivo que o repositório de arquivos do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe07e-182">The Persistent Chat file store uses the same file share as the Lync Server file store.</span></span>

<span data-ttu-id="fe07e-183">Locais do repositório de arquivos são identificados como \\ \\ nome do compartilhamento do servidor \\ .</span><span class="sxs-lookup"><span data-stu-id="fe07e-183">File store locations are identified as \\\\server\\share name.</span></span> <span data-ttu-id="fe07e-184">Para localizar os locais específicos de seus armazenamentos de arquivos, abra o construtor de topologias e procure no nó **armazenamentos de arquivos** .</span><span class="sxs-lookup"><span data-stu-id="fe07e-184">To find the specific locations of your file stores, open Topology Builder and look in the **File stores** node.</span></span>

<span data-ttu-id="fe07e-185">A tabela a seguir identifica os armazenamentos de arquivos que você precisa fazer backup e restaurar.</span><span class="sxs-lookup"><span data-stu-id="fe07e-185">The following table identifies the file stores you need to back up and restore.</span></span>

### <a name="file-stores"></a><span data-ttu-id="fe07e-186">Repositórios de arquivos</span><span class="sxs-lookup"><span data-stu-id="fe07e-186">File Stores</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe07e-187">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fe07e-187">Type of data</span></span></th>
<th><span data-ttu-id="fe07e-188">Onde armazenado</span><span class="sxs-lookup"><span data-stu-id="fe07e-188">Where stored</span></span></th>
<th><span data-ttu-id="fe07e-189">Descrição/quando fazer backup</span><span class="sxs-lookup"><span data-stu-id="fe07e-189">Description / when to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe07e-190">Repositório de arquivos do Lync Server</span><span class="sxs-lookup"><span data-stu-id="fe07e-190">Lync Server file store</span></span></p></td>
<td><p><span data-ttu-id="fe07e-191">Geralmente em um servidor de arquivos, um cluster de arquivos ou um servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="fe07e-191">Typically on a file server, file cluster, or a Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="fe07e-192">Conteúdo da reunião, metadados de conteúdo da reunião, logs de conformidade da reunião, arquivos de dados do aplicativo, arquivos de atualização para atualizações de dispositivo, arquivos de áudio para o grupo de resposta, estacionamento de chamadas e aplicativos de anúncio e arquivos postados em salas de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="fe07e-192">Meeting content, meeting content metadata, meeting compliance logs, application data files, update files for device updates, audio files for Response Group, Call Park, and Announcement applications, and files posted into Persistent Chat rooms.</span></span></p>
<p><span data-ttu-id="fe07e-193">Faça backup com seus backups regulares.</span><span class="sxs-lookup"><span data-stu-id="fe07e-193">Back up with your regular backups.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="additional-backup-requirements"></a><span data-ttu-id="fe07e-194">Requisitos adicionais de backup</span><span class="sxs-lookup"><span data-stu-id="fe07e-194">Additional Backup Requirements</span></span>

<span data-ttu-id="fe07e-195">Para ajudar a garantir a capacidade de restaurar os serviços do Lync Server em caso de falha, você deve fazer backup de alguns componentes necessários que não fazem parte do Lync Server propriamente dito.</span><span class="sxs-lookup"><span data-stu-id="fe07e-195">To help ensure your ability to restore Lync Server services in the event of a failure, you must back up some necessary components that are not part of Lync Server itself.</span></span> <span data-ttu-id="fe07e-196">Não é possível fazer backup ou restauração dos seguintes componentes, como parte do processo de backup e restauração do Lync Server descrito neste documento:</span><span class="sxs-lookup"><span data-stu-id="fe07e-196">The following components are not backed up or restored as part of the Lync Server backup and restoration process described in this document:</span></span>

  - <span data-ttu-id="fe07e-197">**Serviços de domínio do Active Directory**   Você precisa fazer backup do AD DS usando as ferramentas do Active Directory ao mesmo tempo em que fizer backup do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe07e-197">**Active Directory Domain Services**   You need to back up AD DS by using Active Directory tools at the same time that you back up Lync Server.</span></span> <span data-ttu-id="fe07e-198">É importante manter o AD DS sincronizado com o Lync Server para evitar problemas que podem ocorrer quando o Lync Server espera objetos de contato que não correspondem àqueles no AD DS.</span><span class="sxs-lookup"><span data-stu-id="fe07e-198">It is important to keep AD DS synchronized with Lync Server, to avoid problems that can occur when Lync Server expects contact objects that do not match those in AD DS.</span></span> <span data-ttu-id="fe07e-199">O AD DS armazena as seguintes configurações que são usadas pelo Lync Server:</span><span class="sxs-lookup"><span data-stu-id="fe07e-199">AD DS stores the following settings which are used by Lync Server:</span></span>
    
      - <span data-ttu-id="fe07e-200">URI de SIP do usuário e outras configurações do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe07e-200">User SIP URI and other user settings.</span></span>
    
      - <span data-ttu-id="fe07e-201">Objetos de contato para aplicativos como o assistente de grupo de resposta e conferência.</span><span class="sxs-lookup"><span data-stu-id="fe07e-201">Contact objects for applications such as Response Group and Conferencing Attendant.</span></span>
    
      - <span data-ttu-id="fe07e-202">Um ponteiro para o repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="fe07e-202">A pointer to the Central Management Store.</span></span>
    
      - <span data-ttu-id="fe07e-203">Conta de autenticação Kerberos (um objeto de computador opcional) e grupos de segurança do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe07e-203">Kerberos Authentication Account (an optional computer object) and Lync Server security groups.</span></span>
    
    <span data-ttu-id="fe07e-204">Para obter detalhes sobre como fazer backup e restaurar o AD DS no Windows Server 2008, consulte "guia passo a passo de backup e recuperação do AD DS" em [https://go.microsoft.com/fwlink/p/?linkId=209105](https://go.microsoft.com/fwlink/p/?linkid=209105) .</span><span class="sxs-lookup"><span data-stu-id="fe07e-204">For details about backing up and restoring AD DS in Windows Server 2008, see "AD DS Backup and Recovery Step-by-Step Guide" at [https://go.microsoft.com/fwlink/p/?linkId=209105](https://go.microsoft.com/fwlink/p/?linkid=209105).</span></span>

  - <span data-ttu-id="fe07e-205">**Autoridade de certificação e certificados**   Use a política da sua organização para fazer backup da sua CA (autoridade de certificação) e dos certificados.</span><span class="sxs-lookup"><span data-stu-id="fe07e-205">**Certification authority and certificates**   Use your organization's policy for backing up your certification authority (CA) and certificates.</span></span> <span data-ttu-id="fe07e-206">Se você usar chaves privadas exportáveis, poderá fazer backup do certificado e da chave privada e exportá-los se usar os procedimentos deste documento para restaurar o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe07e-206">If you use exportable private keys, you can back up the certificate and the private key, and then export them if you use the procedures in this document to restore Lync Server.</span></span> <span data-ttu-id="fe07e-207">Se você usar uma autoridade de certificação interna, poderá recadastrar se precisar restaurar o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe07e-207">If you use an internal CA, you can re-enroll if you need to restore Lync Server.</span></span> <span data-ttu-id="fe07e-208">É importante manter a chave privada em um local seguro, onde estará disponível se um computador falhar.</span><span class="sxs-lookup"><span data-stu-id="fe07e-208">It is important that you retain the private key in a secure location where it will be available if a computer fails.</span></span>

  - <span data-ttu-id="fe07e-209">**Gerenciador de operações do System Center**   Se você usa o Microsoft System Center Operations Manager (antigo Microsoft Operations Manager) para monitorar a implantação do Lync Server, é possível fazer o backup dos dados que ele cria enquanto estiver monitorando o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe07e-209">**System Center Operations Manager**   If you use Microsoft System Center Operations Manager (formerly Microsoft Operations Manager) to monitor your Lync Server deployment, you can optionally back up the data it creates while it is monitoring Lync Server.</span></span> <span data-ttu-id="fe07e-210">Use o processo de backup padrão do SQL Server para fazer backup dos arquivos do System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="fe07e-210">Use your standard SQL Server backup process to back up System Center Operations Manager files.</span></span> <span data-ttu-id="fe07e-211">Esses arquivos não são restaurados durante a recuperação.</span><span class="sxs-lookup"><span data-stu-id="fe07e-211">These files are not restored during recovery.</span></span>

  - <span data-ttu-id="fe07e-212">**Configuração de gateway PSTN (rede telefônica pública comutada)**   Se você usa utensílios da empresa ou filiais sobreviventes, é preciso fazer backup da configuração do gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="fe07e-212">**Public switched telephone network (PSTN) gateway configuration**   If you use Enterprise Voice or Survivable Branch Appliances, you need to back up the PSTN gateway configuration.</span></span> <span data-ttu-id="fe07e-213">Consulte o fornecedor para obter detalhes sobre como fazer backup e restaurar configurações de gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="fe07e-213">See your vendor for details about backing up and restoring PSTN gateway configurations.</span></span>

  - <span data-ttu-id="fe07e-214">**Versões coexistentes do Lync Server ou do Office Communications Server**   Se sua implantação do Lync Server 2013 existir no Lync Server 2010 ou em uma versão anterior do Office Communications Server, você não poderá usar os procedimentos deste documento para fazer backup ou restaurar a versão anterior.</span><span class="sxs-lookup"><span data-stu-id="fe07e-214">**Coexisting versions of Lync Server or Office Communications Server**   If your Lync Server 2013 deployment coexists with Lync Server 2010 or an earlier version of Office Communications Server, you can’t use the procedures in this document for backing up or restoring the earlier version.</span></span> <span data-ttu-id="fe07e-215">Em vez disso, você deve usar os procedimentos de backup e restauração documentados especificamente para a versão anterior.</span><span class="sxs-lookup"><span data-stu-id="fe07e-215">Instead, you must use the backup and restoration procedures documented specifically for your earlier version.</span></span> <span data-ttu-id="fe07e-216">Para obter detalhes sobre como fazer backup e restaurar o Lync Server 2010, consulte [https://go.microsoft.com/fwlink/p/?linkId=265417](https://go.microsoft.com/fwlink/p/?linkid=265417) .</span><span class="sxs-lookup"><span data-stu-id="fe07e-216">For details about backing up and restoring Lync Server 2010, see [https://go.microsoft.com/fwlink/p/?linkId=265417](https://go.microsoft.com/fwlink/p/?linkid=265417) .</span></span> <span data-ttu-id="fe07e-217">Para obter detalhes sobre como fazer backup e restaurar o Microsoft Office Communications Server 2007 R2, consulte [https://go.microsoft.com/fwlink/p/?linkId=168162](https://go.microsoft.com/fwlink/p/?linkid=168162) .</span><span class="sxs-lookup"><span data-stu-id="fe07e-217">For details about backing up and restoring Microsoft Office Communications Server 2007 R2, see [https://go.microsoft.com/fwlink/p/?linkId=168162](https://go.microsoft.com/fwlink/p/?linkid=168162).</span></span>

  - <span data-ttu-id="fe07e-218">**Informações de infraestrutura**   Você precisa fazer backup de informações sobre sua infraestrutura, como a configuração do seu firewall, a configuração de balanceamento de carga, a configuração de serviços de informações da Internet (IIS), os endereços DNS e os endereços IP e a configuração de protocolo DHCP.</span><span class="sxs-lookup"><span data-stu-id="fe07e-218">**Infrastructure information**   You need to back up information about your infrastructure, such as your firewall configuration, load balancing configuration, Internet Information Services (IIS) configuration, Domain Name System (DNS) records and IP addresses, and Dynamic Host Configuration Protocol (DHCP) configuration.</span></span> <span data-ttu-id="fe07e-219">Para obter detalhes sobre como fazer backup desses componentes, consulte seus respectivos fornecedores.</span><span class="sxs-lookup"><span data-stu-id="fe07e-219">For details about backing up these components, check with their respective vendors.</span></span>

  - <span data-ttu-id="fe07e-220">**Microsoft Exchange e Exchange Unified Messaging (um)**   Fazer backup e restaurar o Microsoft Exchange e o Exchange UM conforme descrito na documentação do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe07e-220">**Microsoft Exchange and Exchange Unified Messaging (UM)**   Backup and restore Microsoft Exchange and Exchange UM as described in the Microsoft Exchange documentation.</span></span> <span data-ttu-id="fe07e-221">Para obter detalhes sobre como fazer backup e restaurar o Exchange Server 2013, consulte [https://go.microsoft.com/fwlink/?LinkId=285384](https://go.microsoft.com/fwlink/?linkid=285384) .</span><span class="sxs-lookup"><span data-stu-id="fe07e-221">For details about backing up and restoring Exchange Server 2013, see [https://go.microsoft.com/fwlink/?LinkId=285384](https://go.microsoft.com/fwlink/?linkid=285384).</span></span> <span data-ttu-id="fe07e-222">Para obter detalhes sobre como fazer backup e restaurar o Exchange Server 2010, consulte [https://go.microsoft.com/fwlink/p/?linkId=209179](https://go.microsoft.com/fwlink/p/?linkid=209179) .</span><span class="sxs-lookup"><span data-stu-id="fe07e-222">For details about backing up and restoring Exchange Server 2010, see [https://go.microsoft.com/fwlink/p/?linkId=209179](https://go.microsoft.com/fwlink/p/?linkid=209179).</span></span>
    
    <span data-ttu-id="fe07e-223">Observe que o Lync Server 2013 introduz a capacidade de ter listas de contatos do usuário, fotos de usuários de alta definição e arquivar dados armazenados no Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="fe07e-223">Note that Lync Server 2013 introduces the ability to have user contact lists, high definition user photos, and archiving data stored in Exchange 2013.</span></span> <span data-ttu-id="fe07e-224">Veja a lista a seguir para ver como fazer backup desses tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="fe07e-224">See the following list to see how to back up these types of data:</span></span>
    
      - <span data-ttu-id="fe07e-225">**Fotos de alta definição** são cofeitas como parte do backup do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fe07e-225">**High definition photos** are backed up as part of the Exchange Server backup.</span></span>
    
      - <span data-ttu-id="fe07e-226">O **repositório de contatos unificado** é apresentado no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fe07e-226">**Unified contact store** is introduced in Lync Server 2013.</span></span> <span data-ttu-id="fe07e-227">O repositório de contatos unificado permite que os usuários mantenham todas as informações de contato no Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="fe07e-227">Unified contact store enables users to keep all their contact information in Exchange 2013.</span></span>
        
        <span data-ttu-id="fe07e-228">Você deve garantir que os backups sejam atualizados para os usuários em termos de se seus contatos do usuário estão armazenados no repositório de contatos unificado ou no servidor do Lync back-end.</span><span class="sxs-lookup"><span data-stu-id="fe07e-228">You should make sure that backups are up-to-date for users in terms of whether their user contacts are stored in the unified contact store or on the Lync Back End Server.</span></span> <span data-ttu-id="fe07e-229">Os cenários a seguir ilustram onde a migração de contatos do usuário para o repositório de contatos unificado pode causar problemas para o processo de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="fe07e-229">The following scenarios illustrate where migrating user contacts to the unified contact store can cause issues for the backup and restore process.</span></span>
        
        <span data-ttu-id="fe07e-230">**Cenário 1:** Os contatos do usuário são migrados para o repositório de contatos unificado, e uma restauração é realizada de um backup do Lync Server feito antes da migração dos contatos do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe07e-230">**Scenario 1:** User contacts are migrated to the unified contact store, and a restore is performed from a Lync Server backup taken prior to the migration of user contacts.</span></span> <span data-ttu-id="fe07e-231">Nesse cenário, o usuário terá um estado de contatos desatualizados para até um dia até que a tarefa de migração do Lync Server comece a migrar contatos do usuário para o Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe07e-231">In this scenario, the user will have a state of outdated contacts for up to one day until Lync Server Migration Task begins migrating user contacts to Exchange.</span></span> <span data-ttu-id="fe07e-232">(Observe que, como os contatos do usuário foram anteriormente migrados para o repositório de contatos unificado, as informações de contato do Exchange serão usadas).</span><span class="sxs-lookup"><span data-stu-id="fe07e-232">(Note that because the user contacts were previously migrated to the unified contact store, the Exchange contact information will be used).</span></span> <span data-ttu-id="fe07e-233">Nesse cenário, nenhuma intervenção do administrador é necessária.</span><span class="sxs-lookup"><span data-stu-id="fe07e-233">No administrator intervention is needed in this scenario.</span></span>
        
        <span data-ttu-id="fe07e-234">**Cenário 2:** Os contatos do usuário foram armazenados anteriormente no repositório de contatos unificado, mas depois revertidos.</span><span class="sxs-lookup"><span data-stu-id="fe07e-234">**Scenario 2:** User contacts were previously stored in the unified contact store, but then rolled back.</span></span> <span data-ttu-id="fe07e-235">Uma restauração é realizada de um backup do Lync Server realizada quando os contatos do usuário eram armazenados no repositório de contatos unificado.</span><span class="sxs-lookup"><span data-stu-id="fe07e-235">A restore is performed from a Lync Server backup taken when the user contacts were stored in the unified contact store.</span></span> <span data-ttu-id="fe07e-236">Nesse cenário, uma mensagem de erro `Error: Incorrect Exchange Version` nos logs do servidor cliente ou Lyss pode indicar isso como um problema.</span><span class="sxs-lookup"><span data-stu-id="fe07e-236">In this scenario, an error message of `Error: Incorrect Exchange Version` in the client or Lyss server logs may indicate this as an issue.</span></span> <span data-ttu-id="fe07e-237">O usuário poderá acessar a lista de contatos no Lync 2013 diretamente do Exchange, mas o estado do cliente não será compatível com o estado do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe07e-237">The user will be able to access their contact list in Lync 2013 directly from Exchange, but client’s state will not match the Lync Server state.</span></span> <span data-ttu-id="fe07e-238">Para corrigir isso, um administrador precisará executar os cmdlets **Invoke-CsUCSRollback** para os usuários afetados.</span><span class="sxs-lookup"><span data-stu-id="fe07e-238">To fix this, an administrator will need to run the **Invoke-CsUCSRollback** cmdlets for the affected users.</span></span>
    
      - <span data-ttu-id="fe07e-239">O **arquivamento de dados** pode ser armazenado no Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="fe07e-239">**Archiving Data** can be stored in Exchange 2013.</span></span> <span data-ttu-id="fe07e-240">Esses dados não são críticos para o Lync Server, mas podem ser críticos para a sua organização para fins reguladores.</span><span class="sxs-lookup"><span data-stu-id="fe07e-240">This data is not critical to Lync Server, but it may be critical to your organization for regulatory purposes.</span></span> <span data-ttu-id="fe07e-241">Se o arquivamento de dados estiver armazenado no Exchange e for essencial para sua organização, siga os procedimentos de backup e restauração do Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe07e-241">If archiving data is stored in Exchange and is critical to your organization, then follow Exchange backup and restore procedures.</span></span> <span data-ttu-id="fe07e-242">Observe que o arquivamento de dados armazenados no Exchange não pode ser retornado ao Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fe07e-242">Note that archiving data stored in Exchange cannot be moved back to Lync Server.</span></span> <span data-ttu-id="fe07e-243">Além disso, não há nenhuma maneira de mover os dados já armazenados no banco de dados de arquivamento do Lync para o Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe07e-243">Additionally, there is no way to move data already stored in the Lync archiving database to Exchange.</span></span>

<span data-ttu-id="fe07e-244"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fe07e-244"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

