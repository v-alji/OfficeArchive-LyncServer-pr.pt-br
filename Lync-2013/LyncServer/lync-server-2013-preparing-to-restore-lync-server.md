---
title: 'Lync Server 2013: preparando para restaurar o Lync Server'
description: 'Lync Server 2013: preparando para restaurar o Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing to restore Lync Server
ms:assetid: 857e4e02-908e-433a-96c6-be1795a9cb61
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202179(v=OCS.15)
ms:contentKeyID: 51541490
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1875a691cfb70a6a824ab19bfde3dee4d699e48a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424090"
---
# <a name="preparing-to-restore-lync-server-2013"></a><span data-ttu-id="3420c-103">Preparando-se para restaurar o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3420c-103">Preparing to restore Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3420c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3420c-104">

<span> </span></span></span>

<span data-ttu-id="3420c-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="3420c-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="3420c-106">Antes de começar a restaurar servidores e bancos de dados após uma falha, você precisa determinar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3420c-106">Before you begin restoring servers and databases after a failure, you need to determine the following:</span></span>

  - <span data-ttu-id="3420c-107">O que precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="3420c-107">What needs to be restored.</span></span>

  - <span data-ttu-id="3420c-108">O hardware, o software, os dados e as ferramentas necessárias para a restauração.</span><span class="sxs-lookup"><span data-stu-id="3420c-108">The hardware, software, data, and tools you need for restoration.</span></span>

<div>

## <a name="determining-what-to-restore"></a><span data-ttu-id="3420c-109">Determinar o que restaurar</span><span class="sxs-lookup"><span data-stu-id="3420c-109">Determining What to Restore</span></span>

<span data-ttu-id="3420c-110">Este tópico descreve como restaurar as quedas do Lync Server que ocorrem no servidor, no pool ou no nível de repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="3420c-110">This topic describes how to restore Lync Server outages that occur at the server, pool, or Central Management store level.</span></span> <span data-ttu-id="3420c-111">Se o repositório de gerenciamento central falhar, a implantação do Lync Server continua a funcionar, mas você não pode fazer alterações de configuração.</span><span class="sxs-lookup"><span data-stu-id="3420c-111">If the Central Management store fails, your Lync Server deployment continues to function, but you cannot make any configuration changes.</span></span> <span data-ttu-id="3420c-112">Se um servidor back-end do servidor ou da edição padrão falhar, o pool de usuários deixará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="3420c-112">If a Back End Server or Standard Edition server fails, the user pool stops functioning.</span></span> <span data-ttu-id="3420c-113">Se qualquer outro servidor falhar, a magnitude da falha dependerá da função do servidor que o servidor está executando e se o servidor hospeda um ou mais bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="3420c-113">If any other server fails, the magnitude of the failure depends on the server role the server is running and whether the server hosts one or more databases.</span></span>

### <a name="what-to-restore"></a><span data-ttu-id="3420c-114">O que restaurar</span><span class="sxs-lookup"><span data-stu-id="3420c-114">What to Restore</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3420c-115">Se isso falhasse</span><span class="sxs-lookup"><span data-stu-id="3420c-115">If this failed</span></span></th>
<th><span data-ttu-id="3420c-116">Consulte esta seção:</span><span class="sxs-lookup"><span data-stu-id="3420c-116">See this section:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3420c-117">Servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="3420c-117">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="3420c-118"><a href="lync-server-2013-restoring-a-standard-edition-server.md">Restaurando um servidor Standard Edition no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3420c-118"><a href="lync-server-2013-restoring-a-standard-edition-server.md">Restoring a Standard Edition server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3420c-119">Repositório de Gerenciamento Central</span><span class="sxs-lookup"><span data-stu-id="3420c-119">Central Management store</span></span></p></td>
<td><p><span data-ttu-id="3420c-120"><a href="lync-server-2013-restoring-the-server-hosting-the-central-management-store.md">Restaurando o servidor que hospeda o repositório de gerenciamento central no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3420c-120"><a href="lync-server-2013-restoring-the-server-hosting-the-central-management-store.md">Restoring the server hosting the Central Management store in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3420c-121">Back-end do Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="3420c-121">Enterprise Edition Back End</span></span></p></td>
<td><p><span data-ttu-id="3420c-122"><a href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">Restaurando um servidor back-end do Enterprise Edition no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3420c-122"><a href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">Restoring an Enterprise Edition Back End Server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3420c-123">Servidor primário de back-end do Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="3420c-123">Enterprise Edition Mirrored Back End Primary Server</span></span></p></td>
<td><p><span data-ttu-id="3420c-124"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md">Restaurando um servidor back-end da edição Enterprise espelhada no Lync Server 2013-principal</a></span><span class="sxs-lookup"><span data-stu-id="3420c-124"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - primary</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3420c-125">Servidor secundário de back-end do Enterprise Edition mirrored</span><span class="sxs-lookup"><span data-stu-id="3420c-125">Enterprise Edition Mirrored Back End Secondary Server</span></span></p></td>
<td><p><span data-ttu-id="3420c-126"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">Restaurando um servidor back-end da edição Enterprise espelhada no Lync Server 2013-Mirror</a></span><span class="sxs-lookup"><span data-stu-id="3420c-126"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3420c-127">Qualquer servidor Enterprise Edition que execute uma função de servidor, como um servidor front-end, servidor de borda, diretor, servidor de mediação ou servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="3420c-127">Any Enterprise Edition server running a server role, such as a Front End Server, Edge Server, Director, Mediation Server,.or Persistent Chat Server.</span></span></p></td>
<td><p><span data-ttu-id="3420c-128"><a href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">Restaurando um servidor membro da Enterprise Edition no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3420c-128"><a href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">Restoring an Enterprise Edition member server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3420c-129">Um pool inteiro do Lync Server</span><span class="sxs-lookup"><span data-stu-id="3420c-129">An entire Lync Server pool</span></span></p></td>
<td><p><span data-ttu-id="3420c-130"><a href="lync-server-2013-restoring-a-lync-server-pool.md">Restaurando um pool do Lync Server no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3420c-130"><a href="lync-server-2013-restoring-a-lync-server-pool.md">Restoring a Lync Server pool in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3420c-131">Repositório de arquivos do Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="3420c-131">Enterprise Edition File Store</span></span></p></td>
<td><p><span data-ttu-id="3420c-132"><a href="lync-server-2013-restoring-a-file-store.md">Restaurando um armazenamento de arquivos no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3420c-132"><a href="lync-server-2013-restoring-a-file-store.md">Restoring a file store in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3420c-133">Um banco de dados de monitoramento autônomo ou um banco de dados de arquivamento</span><span class="sxs-lookup"><span data-stu-id="3420c-133">A standalone Monitoring database or Archiving database</span></span></p></td>
<td><p><span data-ttu-id="3420c-134"><a href="lync-server-2013-restoring-monitoring-or-archiving-data.md">Restaurando o monitoramento ou arquivando dados no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3420c-134"><a href="lync-server-2013-restoring-monitoring-or-archiving-data.md">Restoring monitoring or archiving data in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3420c-135">Um banco de dados persistente de chat autônomo</span><span class="sxs-lookup"><span data-stu-id="3420c-135">A stand-alone Persistent Chat database</span></span></p></td>
<td><p><span data-ttu-id="3420c-136"><a href="lync-server-2013-restoring-persistent-chat-data.md">Restaurando dados de chat persistente no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3420c-136"><a href="lync-server-2013-restoring-persistent-chat-data.md">Restoring Persistent Chat data in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="gathering-hardware-software-and-tools"></a><span data-ttu-id="3420c-137">Reunindo hardware, software e ferramentas</span><span class="sxs-lookup"><span data-stu-id="3420c-137">Gathering Hardware, Software, and Tools</span></span>

<span data-ttu-id="3420c-138">Ao restaurar um servidor, você precisa começar com um computador novo ou limpo.</span><span class="sxs-lookup"><span data-stu-id="3420c-138">When you restore a server, you need to start with a new or clean computer.</span></span> <span data-ttu-id="3420c-139">Além disso, você deve ter os seguintes hardware e software disponíveis:</span><span class="sxs-lookup"><span data-stu-id="3420c-139">Additionally, you must have the following hardware and software available:</span></span>

  - <span data-ttu-id="3420c-140">Um servidor limpo ou novo com o mesmo FQDN (nome de domínio totalmente qualificado) do servidor que falhou.</span><span class="sxs-lookup"><span data-stu-id="3420c-140">A clean or new server with the same fully qualified domain name (FQDN) as the server that failed.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="3420c-141">Ao instalar o sistema operacional, certifique-se de não excluir a conta de computador nos serviços de domínio Active Directory e verifique se as permissões de grupo da conta são mantidas.</span><span class="sxs-lookup"><span data-stu-id="3420c-141">When you install the operating system, make sure that you do not delete the computer account in Active Directory Domain Services, and verify that the group permissions for the account are retained.</span></span>

    
    </div>

  - <span data-ttu-id="3420c-142">Software de instalação para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3420c-142">Installation software for the operating system.</span></span> <span data-ttu-id="3420c-143">Para instalar o sistema operacional, use os procedimentos de implantação do servidor e as configurações estabelecidas pela sua organização.</span><span class="sxs-lookup"><span data-stu-id="3420c-143">To install the operating system, use the server deployment procedures and configurations established by your organization.</span></span> <span data-ttu-id="3420c-144">Você deve ter esses procedimentos e requisitos de configuração disponíveis quando você restaura o serviço.</span><span class="sxs-lookup"><span data-stu-id="3420c-144">You should have these procedures and configuration requirements available when you restore service.</span></span>

  - <span data-ttu-id="3420c-145">Software de instalação do SQL Server 2012 ou do SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="3420c-145">Installation software for SQL Server 2012 or SQL Server 2008 R2.</span></span> <span data-ttu-id="3420c-146">Para instalar um servidor de banco de dados, use a versão apropriada do SQL Server e os procedimentos de implantação do servidor de banco de dados e as configurações estabelecidas pela sua organização.</span><span class="sxs-lookup"><span data-stu-id="3420c-146">To install a database server, use the appropriate version of SQL Server and the database server deployment procedures and configurations established by your organization.</span></span> <span data-ttu-id="3420c-147">Você deve ter esses procedimentos e requisitos de configuração disponíveis quando você restaura o serviço.</span><span class="sxs-lookup"><span data-stu-id="3420c-147">You should have these procedures and configuration requirements available when you restore service.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3420c-148">O assistente de implantação do Lync Server instala automaticamente o SQL Server 2012 Express em cada servidor Standard Edition e em qualquer outro servidor do Lync Server quando um repositório de configuração local é instalado, a menos que você tenha pré-instalado o SQL Server 2012 ou o SQL Server 2008 R2 no servidor.</span><span class="sxs-lookup"><span data-stu-id="3420c-148">The Lync Server Deployment Wizard automatically installs SQL Server 2012 Express on each Standard Edition server and on any other Lync Server server when a local configuration store is installed, unless you have preinstalled SQL Server 2012 or SQL Server 2008 R2 on the server.</span></span>

    
    </div>

  - <span data-ttu-id="3420c-149">Software para fazer imagens do sistema.</span><span class="sxs-lookup"><span data-stu-id="3420c-149">Software for taking system images.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="3420c-150">Recomendamos que você tire uma cópia de imagem do sistema após a instalação do sistema operacional e do SQL Server, e antes de iniciar a restauração, para que você possa usá-la como um ponto de reversão caso algo dê errado durante a restauração.</span><span class="sxs-lookup"><span data-stu-id="3420c-150">We recommend that you take an image copy of the system after you install the operating system and SQL Server, and before you start restoration, so that you can use this image as a rollback point in case something goes wrong during restoration.</span></span>

    
    </div>

  - <span data-ttu-id="3420c-151">Software de instalação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3420c-151">Lync Server 2013 installation software.</span></span> <span data-ttu-id="3420c-152">O assistente de implantação do Lync Server está localizado na pasta de instalação ou mídia do Lync Server na \\ instalação \\ AMD64 \\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="3420c-152">The Lync Server Deployment Wizard is located in the Lync Server installation folder or media at \\setup\\amd64\\Setup.exe.</span></span>

<span data-ttu-id="3420c-153">Durante a restauração, use as seguintes ferramentas:</span><span class="sxs-lookup"><span data-stu-id="3420c-153">During restoration, you use the following tools:</span></span>

  - <span data-ttu-id="3420c-154">Cmdlets do Shell de gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="3420c-154">Lync Server Management Shell cmdlets</span></span>

  - <span data-ttu-id="3420c-155">Import-CsUserData</span><span class="sxs-lookup"><span data-stu-id="3420c-155">Import-CsUserData</span></span>

  - <span data-ttu-id="3420c-156">Ferramentas para restaurar as pastas do Windows</span><span class="sxs-lookup"><span data-stu-id="3420c-156">Tools for restoring Windows folders</span></span>

  - <span data-ttu-id="3420c-157">Construtor de Topologias</span><span class="sxs-lookup"><span data-stu-id="3420c-157">Topology Builder</span></span>

  - <span data-ttu-id="3420c-158">Utilitários de banco de dados do SQL Server, como o SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="3420c-158">SQL Server database utilities, such as SQL Server Management Studio</span></span>

</div>

<div>

## <a name="preparing-to-restore-a-server"></a><span data-ttu-id="3420c-159">Preparando para restaurar um servidor</span><span class="sxs-lookup"><span data-stu-id="3420c-159">Preparing to Restore a Server</span></span>

<span data-ttu-id="3420c-160">Antes de restaurar o servidor, você deve executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="3420c-160">Before you restore the server, you must perform the following steps:</span></span>

1.  <span data-ttu-id="3420c-161">Instale o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3420c-161">Install the operating system.</span></span>

2.  <span data-ttu-id="3420c-162">Se o servidor for um servidor back-end, instale o SQL Server 2012 ou o SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="3420c-162">If the server is a Back End Server, install SQL Server 2012 or SQL Server 2008 R2.</span></span>

3.  <span data-ttu-id="3420c-163">Restaure ou registre novamente seus certificados.</span><span class="sxs-lookup"><span data-stu-id="3420c-163">Restore or reenroll your certificates.</span></span> <span data-ttu-id="3420c-164">Para obter detalhes sobre certificados, consulte "requisitos de backup adicionais" em [requisitos de backup e restauração no Lync Server 2013: dados](lync-server-2013-backup-and-restoration-requirements-data.md).</span><span class="sxs-lookup"><span data-stu-id="3420c-164">For details about certificates, see "Additional Backup Requirements" in [Backup and restoration requirements in Lync Server 2013: data](lync-server-2013-backup-and-restoration-requirements-data.md).</span></span>

4.  <span data-ttu-id="3420c-165">Tire uma imagem do sistema antes de iniciar a restauração para usar como um ponto de recuperação, caso algo dê errado durante a restauração.</span><span class="sxs-lookup"><span data-stu-id="3420c-165">Take an image of the system before starting restoration to use as a rollback point, in case something goes wrong during restoration.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3420c-166">O assistente de implantação do Lync Server e cmdlets descritos nos procedimentos deste tópico e tópicos relacionados, defina todas as listas de controle de acesso (ACLs) necessárias.</span><span class="sxs-lookup"><span data-stu-id="3420c-166">The Lync Server Deployment Wizard and cmdlets described in the procedures in this topic, and related topics, set all required access control lists (ACLs).</span></span>



</div>

<span data-ttu-id="3420c-167">Verifique se o hardware e o software necessários para os componentes que você planeja restaurar estão disponíveis antes de iniciar a restauração.</span><span class="sxs-lookup"><span data-stu-id="3420c-167">Verify that the hardware and the software that you need for the components that you plan to restore are available before you start restoration.</span></span> <span data-ttu-id="3420c-168">Depois de instalar o sistema operacional e o SQL Server, a maioria das etapas nos seguintes procedimentos de restauração podem ser executadas remotamente.</span><span class="sxs-lookup"><span data-stu-id="3420c-168">After you install the operating system and SQL Server, most of the steps in the following restoration procedures can be run remotely.</span></span> <span data-ttu-id="3420c-169">As exceções são observadas nos procedimentos.</span><span class="sxs-lookup"><span data-stu-id="3420c-169">The exceptions are noted in the procedures.</span></span>

<span data-ttu-id="3420c-170">Você também deve ter o plano de backup e restauração da sua organização e as informações do último backup, como as informações nas planilhas deste documento (para obter detalhes, consulte [planilhas de backup e restauração do Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md)), disponíveis antes de começar a restauração.</span><span class="sxs-lookup"><span data-stu-id="3420c-170">You should also have your organization's backup and restoration plan and the information from your last backup, such as the information in the worksheets in this document (for details, see [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md)), available before you begin restoration.</span></span>

<span data-ttu-id="3420c-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3420c-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

