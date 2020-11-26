---
title: 'Lync Server 2013: planilhas de backup e restauração'
description: 'Lync Server 2013: planilhas de backup e restauração.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backup and restoration worksheets
ms:assetid: 26c78155-0306-41ac-845b-7ad58000a1d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202169(v=OCS.15)
ms:contentKeyID: 51541460
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1713e291ae7132cc96309fa499bd97bf7f4f5016
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437956"
---
# <a name="backup-and-restoration-worksheets-for-lync-server-2013"></a><span data-ttu-id="750e2-103">Planilhas de backup e restauração para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="750e2-103">Backup and restoration worksheets for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="750e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="750e2-104">

<span> </span></span></span>

<span data-ttu-id="750e2-105">_**Tópico da última modificação:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="750e2-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="750e2-106">O plano de backup e restauração da sua organização deve conter detalhes sobre como e quando você pode fazer backup de dados e configurações.</span><span class="sxs-lookup"><span data-stu-id="750e2-106">The backup and restoration plan for your organization should contain details about how and when you back up data and settings.</span></span> <span data-ttu-id="750e2-107">Você pode usar as planilhas apresentadas aqui para ajudá-lo a documentar essas informações para sua implantação específica e para os requisitos de backup e restauração da sua organização.</span><span class="sxs-lookup"><span data-stu-id="750e2-107">You can use the worksheets presented here to help you document this information for your specific deployment and for your organization's backup and restoration requirements.</span></span>

<span data-ttu-id="750e2-108">Use as seguintes planilhas para registrar as informações de que você precisa para fazer backup e restaurar o banco de dados, o armazenamento de arquivos e as informações de configurações de um pool de servidores do Lync ou um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="750e2-108">Use the following worksheets to record the information that you need to back up and restore database, File Store, and settings information for a Lync Server pool or Standard Edition server.</span></span> <span data-ttu-id="750e2-109">Mantenha uma ou mais cópias dessas planilhas em um local seguro para que elas fiquem facilmente acessíveis se você precisar restaurar o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="750e2-109">Keep one or more copies of these worksheets in a secure location so that they are readily accessible if you need to restore Lync Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="750e2-110">As planilhas nesta seção abrangem apenas as informações necessárias para restaurar os dados e as configurações dos servidores e bancos de dados do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="750e2-110">The worksheets in this section cover only the information that is required to restore the data and settings of Lync Server databases and servers.</span></span> <span data-ttu-id="750e2-111">Se você precisar documentar outras informações de restauração, como as informações para reinstalar sistemas operacionais e outros softwares, use os planos de implantação da sua organização e os planos de backup e restauração para atender a esses requisitos.</span><span class="sxs-lookup"><span data-stu-id="750e2-111">If you need to document other restoration information, such as the information for reinstalling operating systems and other software, use your organization's deployment plans and backup and restoration plans to address those requirements.</span></span>



</div>

<div>

## <a name="database-backup-and-restoration-worksheet"></a><span data-ttu-id="750e2-112">Planilha de backup e restauração do banco de dados</span><span class="sxs-lookup"><span data-stu-id="750e2-112">Database Backup and Restoration Worksheet</span></span>

<span data-ttu-id="750e2-113">Use a tabela a seguir para registrar as informações de que você precisa para fazer backup e restaurar bancos de dados do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="750e2-113">Use the following table to record the information that you need to back up and restore Lync Server databases.</span></span>

### <a name="database-information-for-backup-and-restoration"></a><span data-ttu-id="750e2-114">Informações de banco de dados para backup e restauração</span><span class="sxs-lookup"><span data-stu-id="750e2-114">Database Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="750e2-115">Base</span><span class="sxs-lookup"><span data-stu-id="750e2-115">Database</span></span></th>
<th><span data-ttu-id="750e2-116">Nome do servidor (FQDN)</span><span class="sxs-lookup"><span data-stu-id="750e2-116">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="750e2-117">Agendamento de backup</span><span class="sxs-lookup"><span data-stu-id="750e2-117">Backup schedule</span></span></th>
<th><span data-ttu-id="750e2-118">Ferramenta de backup do banco de dados</span><span class="sxs-lookup"><span data-stu-id="750e2-118">Database backup tool</span></span></th>
<th><span data-ttu-id="750e2-119">Conjunto de backup</span><span class="sxs-lookup"><span data-stu-id="750e2-119">Backup set</span></span></th>
<th><span data-ttu-id="750e2-120">Destino do backup</span><span class="sxs-lookup"><span data-stu-id="750e2-120">Backup destination</span></span></th>
<th><span data-ttu-id="750e2-121">Observações</span><span class="sxs-lookup"><span data-stu-id="750e2-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="750e2-122">Banco de dados RTC no servidor back-end para dados do usuário</span><span class="sxs-lookup"><span data-stu-id="750e2-122">Rtc database on Back End Server for user data</span></span></p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
<td><p><span data-ttu-id="750e2-123">Cmdlet <strong>Export-CsUserData</strong></span><span class="sxs-lookup"><span data-stu-id="750e2-123"><strong>Export-CsUserData</strong> cmdlet</span></span></p></td>
<td><p><span data-ttu-id="750e2-124">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="750e2-124">Name:</span></span></p>
<p><span data-ttu-id="750e2-125">Expire</span><span class="sxs-lookup"><span data-stu-id="750e2-125">Expiration:</span></span></p>
<p>                   </p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750e2-126">Banco de dados do LcsLog (nome padrão) no servidor de banco de dados de arquivamento</span><span class="sxs-lookup"><span data-stu-id="750e2-126">LcsLog (default name) database on Archiving database server</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="750e2-127">Ferramenta de gerenciamento do SQL Server</span><span class="sxs-lookup"><span data-stu-id="750e2-127">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="750e2-128">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="750e2-128">Name:</span></span></p>
<p><span data-ttu-id="750e2-129">Expire</span><span class="sxs-lookup"><span data-stu-id="750e2-129">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750e2-130">Banco de dados LcsCdr no servidor de banco de dados de monitoramento para registros de detalhes da chamada (CDRs)</span><span class="sxs-lookup"><span data-stu-id="750e2-130">LcsCdr database on Monitoring database server for call detail records (CDRs)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="750e2-131">Ferramenta de gerenciamento do SQL Server</span><span class="sxs-lookup"><span data-stu-id="750e2-131">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="750e2-132">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="750e2-132">Name:</span></span></p>
<p><span data-ttu-id="750e2-133">Expire</span><span class="sxs-lookup"><span data-stu-id="750e2-133">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750e2-134">Banco de dados do QoEMetrics no servidor de banco de dados de monitoramento para dados de qualidade da experiência (QoE)</span><span class="sxs-lookup"><span data-stu-id="750e2-134">QoEMetrics database on Monitoring database server for Quality of Experience (QoE) data</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="750e2-135">Ferramenta de gerenciamento do SQL Server</span><span class="sxs-lookup"><span data-stu-id="750e2-135">SQL Server management tool</span></span></p></td>
<td><p><span data-ttu-id="750e2-136">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="750e2-136">Name:</span></span></p>
<p><span data-ttu-id="750e2-137">Expire</span><span class="sxs-lookup"><span data-stu-id="750e2-137">Expiration:</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750e2-138">Banco de dados de chat persistente</span><span class="sxs-lookup"><span data-stu-id="750e2-138">Persistent Chat Database</span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="750e2-139">Ferramenta de gerenciamento do SQL Server ou cmdlet <strong>Export-CsPersistentChatData</strong></span><span class="sxs-lookup"><span data-stu-id="750e2-139">SQL Server management tool or <strong>Export-CsPersistentChatData</strong> cmdlet</span></span></p></td>
<td><p><span data-ttu-id="750e2-140">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="750e2-140">Name:</span></span></p>
<p><span data-ttu-id="750e2-141">Expire</span><span class="sxs-lookup"><span data-stu-id="750e2-141">Expiration:</span></span></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="750e2-142">Não é necessário backup ou restauração dos seguintes bancos de dados:</span><span class="sxs-lookup"><span data-stu-id="750e2-142">No backup or restoration is required of the following databases:</span></span>

  - <span data-ttu-id="750e2-143">Rtcdyn.</span><span class="sxs-lookup"><span data-stu-id="750e2-143">Rtcdyn.</span></span> <span data-ttu-id="750e2-144">Os dados de usuário transitório nesse banco de dados não são necessários para a restauração do serviço.</span><span class="sxs-lookup"><span data-stu-id="750e2-144">The transient user data in this database is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="750e2-145">Rtcab.</span><span class="sxs-lookup"><span data-stu-id="750e2-145">Rtcab.</span></span> <span data-ttu-id="750e2-146">O banco de dados do catálogo de endereços é automaticamente recriado a partir da lista de endereços global (GAL) nos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="750e2-146">The Address Book database is automatically recreated from the Global Address List (GAL) in Active Directory Domain Services.</span></span>

  - <span data-ttu-id="750e2-147">Rgsdyn.</span><span class="sxs-lookup"><span data-stu-id="750e2-147">Rgsdyn.</span></span> <span data-ttu-id="750e2-148">Os dados do serviço de grupo de resposta transitório nesse banco de dados não são necessários para a restauração do serviço.</span><span class="sxs-lookup"><span data-stu-id="750e2-148">The transient Response Group service data in this database is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="750e2-149">Cpsdyn.</span><span class="sxs-lookup"><span data-stu-id="750e2-149">Cpsdyn.</span></span> <span data-ttu-id="750e2-150">As informações dinâmicas do aplicativo de estacionamento de chamadas não são necessárias para a restauração do serviço.</span><span class="sxs-lookup"><span data-stu-id="750e2-150">The dynamic information for the Call Park application is not necessary for restoration of service.</span></span>

  - <span data-ttu-id="750e2-151">MgcComp.</span><span class="sxs-lookup"><span data-stu-id="750e2-151">MgcComp.</span></span> <span data-ttu-id="750e2-152">O banco de dados de conformidade para chat persistente não é necessário para a restauração do serviço.</span><span class="sxs-lookup"><span data-stu-id="750e2-152">The compliance database for Persistent Chat is not necessary for restoration of service.</span></span>

</div>

<div>

## <a name="file-store-backup-and-restoration-worksheet"></a><span data-ttu-id="750e2-153">Planilha de backup e restauração do repositório de arquivos</span><span class="sxs-lookup"><span data-stu-id="750e2-153">File Store Backup and Restoration Worksheet</span></span>

<span data-ttu-id="750e2-154">Use a tabela a seguir para registrar as informações de que você precisa para fazer backup e restaurar os repositórios de arquivos.</span><span class="sxs-lookup"><span data-stu-id="750e2-154">Use the following table to record the information that you need to back up and restore the File Stores.</span></span> <span data-ttu-id="750e2-155">Os repositórios de arquivos contêm dados como metadados de conteúdo da reunião, logs de conformidade da reunião, logs de atualização para atualizações de dispositivos e arquivos de áudio para o grupo de resposta, o estacionamento de chamadas e os aplicativos de anúncio.</span><span class="sxs-lookup"><span data-stu-id="750e2-155">File Stores contain data such as meeting content metadata, meeting compliance logs, update logs for device updates, and audio files for the Response Group, Call Park, and Announcement applications.</span></span>

### <a name="file-store-information-for-backup-and-restoration"></a><span data-ttu-id="750e2-156">Informações do repositório de arquivos para backup e restauração</span><span class="sxs-lookup"><span data-stu-id="750e2-156">File Store Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="750e2-157">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="750e2-157">Content</span></span></th>
<th><span data-ttu-id="750e2-158">Nome do servidor (FQDN)</span><span class="sxs-lookup"><span data-stu-id="750e2-158">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="750e2-159">Agendamento de backup</span><span class="sxs-lookup"><span data-stu-id="750e2-159">Backup schedule</span></span></th>
<th><span data-ttu-id="750e2-160">Ferramenta de backup do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="750e2-160">File system backup tool</span></span></th>
<th><span data-ttu-id="750e2-161">Compartilhamento de arquivos para backup \*</span><span class="sxs-lookup"><span data-stu-id="750e2-161">File share to be backed up \*</span></span></th>
<th><span data-ttu-id="750e2-162">Destino do backup</span><span class="sxs-lookup"><span data-stu-id="750e2-162">Backup destination</span></span></th>
<th><span data-ttu-id="750e2-163">Observações</span><span class="sxs-lookup"><span data-stu-id="750e2-163">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="750e2-164">Repositório de arquivos do Lync Server</span><span class="sxs-lookup"><span data-stu-id="750e2-164">Lync Server File Store</span></span></p></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="750e2-165">Ferramenta de backup padrão, como Robocopy</span><span class="sxs-lookup"><span data-stu-id="750e2-165">Standard backup tool, such as Robocopy</span></span></p></td>
<td><p><span data-ttu-id="750e2-166">No servidor de arquivos para Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="750e2-166">On file server for Enterprise Edition.</span></span> <span data-ttu-id="750e2-167">Na Standard Edition por padrão, para implantação de edição padrão.</span><span class="sxs-lookup"><span data-stu-id="750e2-167">On Standard Edition by default, for Standard Edition deployment.</span></span> <span data-ttu-id="750e2-168">Geralmente, um por site.</span><span class="sxs-lookup"><span data-stu-id="750e2-168">Typically, one per site.</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="750e2-169">Arquivos chamados <strong>Meeting. Active</strong> não devem ser backups.</span><span class="sxs-lookup"><span data-stu-id="750e2-169">Files named <strong>Meeting.Active</strong> should not be backed up.</span></span> <span data-ttu-id="750e2-170">Esses arquivos estão em uso e são bloqueados durante o momento em que uma reunião ocorre.</span><span class="sxs-lookup"><span data-stu-id="750e2-170">These files are in use and are locked while a meeting takes place.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="settings-backup-and-restoration-worksheet"></a><span data-ttu-id="750e2-171">Configurar a planilha de backup e restauração</span><span class="sxs-lookup"><span data-stu-id="750e2-171">Settings Backup and Restoration Worksheet</span></span>

<span data-ttu-id="750e2-172">Use a tabela a seguir para registrar as informações de que você precisa para fazer backup e restaurar as configurações.</span><span class="sxs-lookup"><span data-stu-id="750e2-172">Use the following table to record the information that you need to back up and restore settings.</span></span>

### <a name="settings-information-for-backup-and-restoration"></a><span data-ttu-id="750e2-173">Informações de configuração para backup e restauração</span><span class="sxs-lookup"><span data-stu-id="750e2-173">Settings Information for Backup and Restoration</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="750e2-174">Base</span><span class="sxs-lookup"><span data-stu-id="750e2-174">Database</span></span></th>
<th><span data-ttu-id="750e2-175">Nome do servidor (FQDN)</span><span class="sxs-lookup"><span data-stu-id="750e2-175">Server name (FQDN)</span></span></th>
<th><span data-ttu-id="750e2-176">Agendamento de backup</span><span class="sxs-lookup"><span data-stu-id="750e2-176">Backup schedule</span></span></th>
<th><span data-ttu-id="750e2-177">Ferramenta de backup</span><span class="sxs-lookup"><span data-stu-id="750e2-177">Backup tool</span></span></th>
<th><span data-ttu-id="750e2-178">Nome do arquivo de configuração (. xml)</span><span class="sxs-lookup"><span data-stu-id="750e2-178">Configuration file (.xml) name</span></span></th>
<th><span data-ttu-id="750e2-179">Local do backup</span><span class="sxs-lookup"><span data-stu-id="750e2-179">Backup location</span></span></th>
<th><span data-ttu-id="750e2-180">Observações</span><span class="sxs-lookup"><span data-stu-id="750e2-180">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="750e2-181">Banco de dados XDS no repositório de gerenciamento central para configuração de topologia (global)</span><span class="sxs-lookup"><span data-stu-id="750e2-181">Xds database in Central Management store for topology configuration (global)</span></span></p></td>
<td><p>                    </p></td>
<td><p>                    </p></td>
<td><p><span data-ttu-id="750e2-182">Cmdlet <strong>Export-CsConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="750e2-182"><strong>Export-CsConfiguration</strong> cmdlet</span></span></p></td>
<td><p>                   </p></td>
<td><p>                    </p></td>
<td><p>                   </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="750e2-183">Lis o banco de dados no repositório de gerenciamento central para E9-1-1 informações de localização (global)</span><span class="sxs-lookup"><span data-stu-id="750e2-183">Lis database in Central Management store for E9-1-1 location information (global)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="750e2-184">Cmdlet <strong>Export-CsLisConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="750e2-184"><strong>Export-CsLisConfiguration</strong> cmdlet</span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p>                    </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="750e2-185">Banco de dados do RgsConfig no servidor back-end para configuração de grupo de resposta (pool)</span><span class="sxs-lookup"><span data-stu-id="750e2-185">RgsConfig database on Back End Server for Response Group configuration (pool)</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="750e2-186">Cmdlet <strong>Export-CsRgsConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="750e2-186"><strong>Export-CsRgsConfiguration</strong> cmdlet</span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p>                    </p></td>
</tr>
</tbody>
</table><span data-ttu-id="750e2-187">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="750e2-187">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

