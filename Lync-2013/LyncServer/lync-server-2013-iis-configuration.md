---
title: 'Lync Server 2013: Configuração de IIS'
description: 'Lync Server 2013: configuração do IIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IIS configuration
ms:assetid: b458babf-bf64-43f0-8a8e-612f5096b63c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412871(v=OCS.15)
ms:contentKeyID: 48185169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 901aca7bf5ff8824b54e93754569a6ef5defc10e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427429"
---
# <a name="iis-configuration-in-lync-server-2013"></a><span data-ttu-id="7aff5-103">Configuração de IIS no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7aff5-103">IIS configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7aff5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7aff5-104">

<span> </span></span></span>

<span data-ttu-id="7aff5-105">_**Tópico da última modificação:** 2014-02-17_</span><span class="sxs-lookup"><span data-stu-id="7aff5-105">_**Topic Last Modified:** 2014-02-17_</span></span>

<span data-ttu-id="7aff5-106">Para concluir esse procedimento com êxito, você deve estar conectado ao servidor minimamente como um administrador local e um usuário do domínio.</span><span class="sxs-lookup"><span data-stu-id="7aff5-106">To successfully complete this procedure, you should be logged on to the server minimally as a local administrator and a domain user.</span></span>

<span data-ttu-id="7aff5-107">Antes de configurar e instalar o servidor front-end para o Lync Server 2013, Standard Edition ou o primeiro servidor front-end em um pool, instale e configure a função do servidor e os serviços Web para serviços de informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="7aff5-107">Before you configure and install the Front End Server for Lync Server 2013, Standard Edition or the first Front End Server in a pool, you install and configure the server role and Web Services for Internet Information Services (IIS).</span></span>

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="7aff5-108">Se a sua organização exigir que você localize o IIS e todos os serviços Web em uma unidade diferente da unidade do sistema, você poderá alterar o caminho do local de instalação dos arquivos do Lync Server 2013 na caixa de diálogo Configurar ao instalar inicialmente as ferramentas administrativas do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7aff5-108">If your organization requires that you locate IIS and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server 2013 files in the Setup dialog box when you initially install the Lync Server 2013 Administrative tools.</span></span> <span data-ttu-id="7aff5-109">Instale as ferramentas administrativas antes de instalar o IIS.</span><span class="sxs-lookup"><span data-stu-id="7aff5-109">You install the Administrative tools before installing IIS.</span></span> <span data-ttu-id="7aff5-110">Se você instalar os arquivos de instalação nesse caminho, incluindo OCSCore.msi, o restante dos arquivos do Lync Server 2013 também será implantado nessa unidade.</span><span class="sxs-lookup"><span data-stu-id="7aff5-110">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will be deployed to this drive as well.</span></span> <span data-ttu-id="7aff5-111">Para o dtails, confira <A href="lync-server-2013-install-lync-server-administrative-tools.md">instalar as ferramentas administrativas do Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7aff5-111">For dtails, see <A href="lync-server-2013-install-lync-server-administrative-tools.md">Install Lync Server 2013 administrative tools</A>.</span></span> <span data-ttu-id="7aff5-112">Para obter detalhes sobre como realocar o INETPUB implantado pelo Windows Server Manager ao instalar o IIS, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A> .</span><span class="sxs-lookup"><span data-stu-id="7aff5-112">For details about how to relocate the INETPUB deployed by Windows Server Manager when installing IIS, see <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A>.</span></span>



</div>

<span data-ttu-id="7aff5-113">A tabela a seguir indica os serviços de função do IIS 7,5 necessários.</span><span class="sxs-lookup"><span data-stu-id="7aff5-113">The following table indicates the required IIS 7.5 role services.</span></span>

### <a name="iis-75-role-services"></a><span data-ttu-id="7aff5-114">Serviços de função do IIS 7,5</span><span class="sxs-lookup"><span data-stu-id="7aff5-114">IIS 7.5 Role Services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7aff5-115">Título da função</span><span class="sxs-lookup"><span data-stu-id="7aff5-115">Role Heading</span></span></th>
<th><span data-ttu-id="7aff5-116">Serviço de função</span><span class="sxs-lookup"><span data-stu-id="7aff5-116">Role Service</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-117">Recursos comuns de HTTP instalados</span><span class="sxs-lookup"><span data-stu-id="7aff5-117">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="7aff5-118">Conteúdo estático</span><span class="sxs-lookup"><span data-stu-id="7aff5-118">Static content</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-119">Recursos comuns de HTTP instalados</span><span class="sxs-lookup"><span data-stu-id="7aff5-119">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="7aff5-120">Documento padrão</span><span class="sxs-lookup"><span data-stu-id="7aff5-120">Default document</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-121">Recursos comuns de HTTP instalados</span><span class="sxs-lookup"><span data-stu-id="7aff5-121">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="7aff5-122">Erros de HTTP</span><span class="sxs-lookup"><span data-stu-id="7aff5-122">HTTP errors</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-123">Desenvolvimento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="7aff5-123">Application development</span></span></p></td>
<td><p><span data-ttu-id="7aff5-124">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="7aff5-124">ASP.NET</span></span></p>
<p><span data-ttu-id="7aff5-125">O Windows Server 2012 também requer o ASP. NET 4.5</span><span class="sxs-lookup"><span data-stu-id="7aff5-125">Windows Server 2012 also requires ASP.NET4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-126">Desenvolvimento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="7aff5-126">Application development</span></span></p></td>
<td><p><span data-ttu-id="7aff5-127">Extensibilidade .NET</span><span class="sxs-lookup"><span data-stu-id="7aff5-127">.NET extensibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-128">Desenvolvimento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="7aff5-128">Application development</span></span></p></td>
<td><p><span data-ttu-id="7aff5-129">Extensões da API de servidor da Internet (ISAPI)</span><span class="sxs-lookup"><span data-stu-id="7aff5-129">Internet Server API (ISAPI) extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-130">Desenvolvimento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="7aff5-130">Application development</span></span></p></td>
<td><p><span data-ttu-id="7aff5-131">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="7aff5-131">ISAPI filters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-132">Integridade e diagnóstico</span><span class="sxs-lookup"><span data-stu-id="7aff5-132">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="7aff5-133">Log HTTP</span><span class="sxs-lookup"><span data-stu-id="7aff5-133">HTTP logging</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-134">Integridade e diagnóstico</span><span class="sxs-lookup"><span data-stu-id="7aff5-134">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="7aff5-135">Ferramentas de log</span><span class="sxs-lookup"><span data-stu-id="7aff5-135">Logging tools</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-136">Integridade e diagnóstico</span><span class="sxs-lookup"><span data-stu-id="7aff5-136">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="7aff5-137">Rastreamento</span><span class="sxs-lookup"><span data-stu-id="7aff5-137">Tracing</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-138">Segurança</span><span class="sxs-lookup"><span data-stu-id="7aff5-138">Security</span></span></p></td>
<td><p><span data-ttu-id="7aff5-139">Autenticação anônima (instalada e habilitada por padrão)</span><span class="sxs-lookup"><span data-stu-id="7aff5-139">Anonymous authentication (installed and enabled by default)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-140">Segurança</span><span class="sxs-lookup"><span data-stu-id="7aff5-140">Security</span></span></p></td>
<td><p><span data-ttu-id="7aff5-141">Autenticação do Windows</span><span class="sxs-lookup"><span data-stu-id="7aff5-141">Windows authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-142">Segurança</span><span class="sxs-lookup"><span data-stu-id="7aff5-142">Security</span></span></p></td>
<td><p><span data-ttu-id="7aff5-143">Autenticação de mapeamento de certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="7aff5-143">Client Certificate Mapping authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-144">Segurança</span><span class="sxs-lookup"><span data-stu-id="7aff5-144">Security</span></span></p></td>
<td><p><span data-ttu-id="7aff5-145">Filtragem de solicitações</span><span class="sxs-lookup"><span data-stu-id="7aff5-145">Request filtering</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-146">Desempenho</span><span class="sxs-lookup"><span data-stu-id="7aff5-146">Performance</span></span></p></td>
<td><p><span data-ttu-id="7aff5-147">Compactação de conteúdo estático</span><span class="sxs-lookup"><span data-stu-id="7aff5-147">Static content compression</span></span></p>
<p><span data-ttu-id="7aff5-148">Compactação de conteúdo dinâmico</span><span class="sxs-lookup"><span data-stu-id="7aff5-148">Dynamic content compression</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-149">Ferramentas de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7aff5-149">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="7aff5-150">Console de gerenciamento IIS</span><span class="sxs-lookup"><span data-stu-id="7aff5-150">IIS Management Console</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-151">Ferramentas de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7aff5-151">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="7aff5-152">Ferramentas e scripts de gerenciamento IIS</span><span class="sxs-lookup"><span data-stu-id="7aff5-152">IIS Management Scripts and Tools</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7aff5-153">No sistema operacional Windows Server 2008 R2 SP1 x64, você pode usar o Windows PowerShell 2,0.</span><span class="sxs-lookup"><span data-stu-id="7aff5-153">On the Windows Server 2008 R2 SP1 x64 operating system, you can use Windows PowerShell 2.0.</span></span> <span data-ttu-id="7aff5-154">Primeiro, você deve importar o módulo ServerManager e instalar os serviços de função e função do IIS 7,5.</span><span class="sxs-lookup"><span data-stu-id="7aff5-154">You must first import the ServerManager module, and then install the IIS 7.5 role and role services.</span></span>

   ```PowerShell
    Import-Module ServerManager
   ```

   ```PowerShell
    Add-WindowsFeature Web-Server, Web-Static-Content, Web-Default-Doc, Web-Scripting-Tools, Web-Windows-Auth, Web-Asp-Net, Web-Log-Libraries, Web-Http-Tracing, Web-Stat-Compression, Web-Dyn-Compression, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Errors, Web-Http-Logging, Web-Net-Ext, Web-Client-Auth, Web-Filtering, Web-Mgmt-Console
   ```

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="7aff5-155">A autenticação anônima é instalada por padrão com a função de servidor IIS.</span><span class="sxs-lookup"><span data-stu-id="7aff5-155">Anonymous authentication is installed by default with the IIS server role.</span></span> <span data-ttu-id="7aff5-156">Você pode gerenciar a autenticação anônima após a instalação do IIS.</span><span class="sxs-lookup"><span data-stu-id="7aff5-156">You can manage anonymous authentication after the installation of IIS.</span></span> <span data-ttu-id="7aff5-157">Para obter detalhes, consulte "habilitar autenticação anônima (IIS 7)" em <A href="https://go.microsoft.com/fwlink/p/?linkid=203935">https://go.microsoft.com/fwlink/p/?linkId=203935</A> .</span><span class="sxs-lookup"><span data-stu-id="7aff5-157">For details, see “Enable Anonymous Authentication (IIS 7)” at <A href="https://go.microsoft.com/fwlink/p/?linkid=203935">https://go.microsoft.com/fwlink/p/?linkId=203935</A>.</span></span>



</div>

<span data-ttu-id="7aff5-158">A tabela a seguir indica os serviços de função do IIS 8,0 e do IIS 8,5 necessários para o Windows Server 2012 e o Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="7aff5-158">The following table indicates the required IIS 8.0 and IIS 8.5 role services for Windows Server 2012 and Windows Server 2012 R2.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="7aff5-159">Para o Windows Server 2012 e o Windows Server 2012 R2, o cmdlet Add-WindowsFeature foi substituído pelo cmdlet Install-WindowsFeature.</span><span class="sxs-lookup"><span data-stu-id="7aff5-159">For Windows Server 2012 and Windows Server 2012 R2, the Add-WindowsFeature cmdlet has been replaced by the Install-WindowsFeature cmdlet.</span></span> <span data-ttu-id="7aff5-160">Para obter detalhes, consulte <A href="https://go.microsoft.com/fwlink/p/?linkid=392274">install-WindowsFeature</A>.</span><span class="sxs-lookup"><span data-stu-id="7aff5-160">For details, see <A href="https://go.microsoft.com/fwlink/p/?linkid=392274">Install-WindowsFeature</A>.</span></span>



</div>

### <a name="iis-80-and-iis-85-role-services"></a><span data-ttu-id="7aff5-161">Serviços de função do IIS 8,0 e do IIS 8,5</span><span class="sxs-lookup"><span data-stu-id="7aff5-161">IIS 8.0 and IIS 8.5 Role Services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7aff5-162">Título da função</span><span class="sxs-lookup"><span data-stu-id="7aff5-162">Role Heading</span></span></th>
<th><span data-ttu-id="7aff5-163">Serviço de função</span><span class="sxs-lookup"><span data-stu-id="7aff5-163">Role Service</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-164">Servidor Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="7aff5-164">Web Server (IIS)</span></span></p></td>
<td><p><span data-ttu-id="7aff5-165">Servidor Web</span><span class="sxs-lookup"><span data-stu-id="7aff5-165">Web Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-166">Recursos HTTP Comuns</span><span class="sxs-lookup"><span data-stu-id="7aff5-166">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="7aff5-167">Documento padrão</span><span class="sxs-lookup"><span data-stu-id="7aff5-167">Default Document</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-168">Recursos HTTP Comuns</span><span class="sxs-lookup"><span data-stu-id="7aff5-168">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="7aff5-169">Pesquisa de diretório</span><span class="sxs-lookup"><span data-stu-id="7aff5-169">Directory Browsing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-170">Recursos HTTP Comuns</span><span class="sxs-lookup"><span data-stu-id="7aff5-170">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="7aff5-171">Erros HTTP</span><span class="sxs-lookup"><span data-stu-id="7aff5-171">HTTP Errors</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-172">Recursos HTTP Comuns</span><span class="sxs-lookup"><span data-stu-id="7aff5-172">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="7aff5-173">Conteúdo estático</span><span class="sxs-lookup"><span data-stu-id="7aff5-173">Static content</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-174">Recursos HTTP Comuns</span><span class="sxs-lookup"><span data-stu-id="7aff5-174">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="7aff5-175">Redirecionamento de HTTP</span><span class="sxs-lookup"><span data-stu-id="7aff5-175">HTTP Redirection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-176">Integridade e Diagnósticos</span><span class="sxs-lookup"><span data-stu-id="7aff5-176">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="7aff5-177">Log HTTP</span><span class="sxs-lookup"><span data-stu-id="7aff5-177">HTTP Logging</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-178">Integridade e Diagnósticos</span><span class="sxs-lookup"><span data-stu-id="7aff5-178">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="7aff5-179">Ferramentas de log</span><span class="sxs-lookup"><span data-stu-id="7aff5-179">Logging Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-180">Integridade e Diagnósticos</span><span class="sxs-lookup"><span data-stu-id="7aff5-180">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="7aff5-181">Monitor de solicitação</span><span class="sxs-lookup"><span data-stu-id="7aff5-181">Request Monitor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-182">Integridade e Diagnósticos</span><span class="sxs-lookup"><span data-stu-id="7aff5-182">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="7aff5-183">Rastreamento</span><span class="sxs-lookup"><span data-stu-id="7aff5-183">Tracing</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-184">Segurança</span><span class="sxs-lookup"><span data-stu-id="7aff5-184">Security</span></span></p></td>
<td><p><span data-ttu-id="7aff5-185">Requisição de filtro</span><span class="sxs-lookup"><span data-stu-id="7aff5-185">Request Filtering</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-186">Segurança</span><span class="sxs-lookup"><span data-stu-id="7aff5-186">Security</span></span></p></td>
<td><p><span data-ttu-id="7aff5-187">Autenticação básica</span><span class="sxs-lookup"><span data-stu-id="7aff5-187">Basic Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-188">Segurança</span><span class="sxs-lookup"><span data-stu-id="7aff5-188">Security</span></span></p></td>
<td><p><span data-ttu-id="7aff5-189">Autenticação de mapeamento de certificado de cliente</span><span class="sxs-lookup"><span data-stu-id="7aff5-189">Client Certificate Mapping Authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-190">Segurança</span><span class="sxs-lookup"><span data-stu-id="7aff5-190">Security</span></span></p></td>
<td><p><span data-ttu-id="7aff5-191">Autenticação do Windows</span><span class="sxs-lookup"><span data-stu-id="7aff5-191">Windows Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-192">Desenvolvimento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7aff5-192">Application Development</span></span></p></td>
<td><p><span data-ttu-id="7aff5-193">.Net Extensibility 3,5</span><span class="sxs-lookup"><span data-stu-id="7aff5-193">.Net Extensibility 3.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-194">Desenvolvimento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7aff5-194">Application Development</span></span></p></td>
<td><p><span data-ttu-id="7aff5-195">.Net Extensibility 4,5</span><span class="sxs-lookup"><span data-stu-id="7aff5-195">.Net Extensibility 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-196">Desenvolvimento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7aff5-196">Application Development</span></span></p></td>
<td><p><span data-ttu-id="7aff5-197">ASP.Net 3,5</span><span class="sxs-lookup"><span data-stu-id="7aff5-197">ASP.Net 3.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-198">Desenvolvimento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7aff5-198">Application Development</span></span></p></td>
<td><p><span data-ttu-id="7aff5-199">ASP.Net 4,5</span><span class="sxs-lookup"><span data-stu-id="7aff5-199">ASP.Net 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-200">Desenvolvimento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7aff5-200">Application Development</span></span></p></td>
<td><p><span data-ttu-id="7aff5-201">Extensões ISAPI</span><span class="sxs-lookup"><span data-stu-id="7aff5-201">ISAPI Extensions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-202">Desenvolvimento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7aff5-202">Application Development</span></span></p></td>
<td><p><span data-ttu-id="7aff5-203">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="7aff5-203">ISAPI Filters</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-204">Desenvolvimento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7aff5-204">Application Development</span></span></p></td>
<td><p><span data-ttu-id="7aff5-205">Inclusões do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="7aff5-205">Server Side Includes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-206">Ferramentas de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7aff5-206">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="7aff5-207">Console de gerenciamento IIS</span><span class="sxs-lookup"><span data-stu-id="7aff5-207">IIS Management Console</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-208">Ferramentas de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7aff5-208">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="7aff5-209">Compatibilidade de metabase do IIS 6</span><span class="sxs-lookup"><span data-stu-id="7aff5-209">IIS 6 Metabase compatibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-210">Ferramentas de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7aff5-210">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="7aff5-211">Ferramentas e scripts de gerenciamento IIS</span><span class="sxs-lookup"><span data-stu-id="7aff5-211">IIS Management Scripts and Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-212">Recursos da .net 3,5 Framework</span><span class="sxs-lookup"><span data-stu-id="7aff5-212">.Net 3.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="7aff5-213">.Net 3,5 Framework</span><span class="sxs-lookup"><span data-stu-id="7aff5-213">.Net 3.5 Framework</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-214">Recursos da .NET 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="7aff5-214">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="7aff5-215">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="7aff5-215">.Net Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-216">Recursos da .NET 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="7aff5-216">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="7aff5-217">ASP.Net 4,5</span><span class="sxs-lookup"><span data-stu-id="7aff5-217">ASP.Net 4.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-218">Recursos da .NET 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="7aff5-218">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="7aff5-219">Ativação HTTP</span><span class="sxs-lookup"><span data-stu-id="7aff5-219">HTTP Activation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-220">Recursos da .NET 4,5 Framework</span><span class="sxs-lookup"><span data-stu-id="7aff5-220">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="7aff5-221">Compartilhamento de porta TCP</span><span class="sxs-lookup"><span data-stu-id="7aff5-221">TCP Port Sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-222">Serviço de transferência inteligente em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7aff5-222">Background Intelligent Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="7aff5-223">Extensões de servidor IIS</span><span class="sxs-lookup"><span data-stu-id="7aff5-223">IIS Server Extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-224">Serviços de tinta e manuscrito</span><span class="sxs-lookup"><span data-stu-id="7aff5-224">Ink and Handwriting Services</span></span></p></td>
<td><p><span data-ttu-id="7aff5-225">Serviços de tinta e manuscrito</span><span class="sxs-lookup"><span data-stu-id="7aff5-225">Ink and Handwriting Services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-226">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7aff5-226">Media Foundation</span></span></p></td>
<td><p><span data-ttu-id="7aff5-227">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7aff5-227">Media Foundation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-228">Interfaces do usuário e infraestrutura</span><span class="sxs-lookup"><span data-stu-id="7aff5-228">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="7aff5-229">Infraestrutura e ferramentas de gerenciamento gráfico</span><span class="sxs-lookup"><span data-stu-id="7aff5-229">Graphical Management Tools and Infrastructure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-230">Interfaces do usuário e infraestrutura</span><span class="sxs-lookup"><span data-stu-id="7aff5-230">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="7aff5-231">Experiência Desktop</span><span class="sxs-lookup"><span data-stu-id="7aff5-231">Desktop Experience</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-232">Interfaces do usuário e infraestrutura</span><span class="sxs-lookup"><span data-stu-id="7aff5-232">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="7aff5-233">Shell gráfico do servidor</span><span class="sxs-lookup"><span data-stu-id="7aff5-233">Server Graphical Shell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-234">Windows Identity Foundation 3.5</span><span class="sxs-lookup"><span data-stu-id="7aff5-234">Windows Identity Foundation 3.5</span></span></p></td>
<td><p><span data-ttu-id="7aff5-235">Windows Identity Foundation 3.5</span><span class="sxs-lookup"><span data-stu-id="7aff5-235">Windows Identity Foundation 3.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7aff5-236">Serviço de ativação de processos do Windows</span><span class="sxs-lookup"><span data-stu-id="7aff5-236">Windows Process Activation Service</span></span></p></td>
<td><p><span data-ttu-id="7aff5-237">Modelo de processo</span><span class="sxs-lookup"><span data-stu-id="7aff5-237">Process Model</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7aff5-238">Serviço de ativação de processos do Windows</span><span class="sxs-lookup"><span data-stu-id="7aff5-238">Windows Process Activation Service</span></span></p></td>
<td><p><span data-ttu-id="7aff5-239">APIs de configuração</span><span class="sxs-lookup"><span data-stu-id="7aff5-239">Configuration APIs</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7aff5-240">No Windows Server 2012 e no Windows Server 2012 R2, você pode usar o Windows PowerShell 3,0 para instalar os requisitos do IIS.</span><span class="sxs-lookup"><span data-stu-id="7aff5-240">In Windows Server 2012 and Windows Server 2012 R2, you can use Windows PowerShell 3.0 to install the IIS Requirements.</span></span> <span data-ttu-id="7aff5-241">Usando o módulo ServerManager no Windows PowerShell 3,0, digite:</span><span class="sxs-lookup"><span data-stu-id="7aff5-241">Using the ServerManager module in Windows PowerShell 3.0, type:</span></span>

   ```PowerShell
    Import-Module ServerManager
   ```

   ```PowerShell
    Add-WindowsFeature Web-Server, Web-Static-Content, Web-Default-Doc, Web-Http-Errors, Web-Asp-Net, Web-Net-Ext, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Logging, Web-Log-Libraries, Web-Request-Monitor, Web-Http-Tracing, Web-Basic-Auth, Web-Windows-Auth, Web-Client-Auth, Web-Filtering, Web-Stat-Compression, Web-Dyn-Compression, NET-Framework-45-Core, NET-WCF-HTTP-Activation45, Web-Asp-Net45, Web-Mgmt-Tools, Web-Scripting-Tools, Web-Mgmt-Console, Web-Mgmt-Compat, Windows-Identity-Foundation, Server-Media-Foundation, BITS -Source D:\sources\sxs
   ```

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="7aff5-242">Novo com o Windows Server 2012 é o parâmetro-source que define onde a mídia de origem do Windows Server 2012 pode ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="7aff5-242">New with Windows Server 2012 is the –Source parameter that defines where the Windows Server 2012 source media can be found.</span></span> <span data-ttu-id="7aff5-243">A mídia pode ser definida como uma unidade de DVD (por exemplo, D:\Sources\Sxs) ou em um compartilhamento de rede em que os arquivos de mídia foram copiados (por exemplo, \\ fileserver\windows2012\sources\Sxs).</span><span class="sxs-lookup"><span data-stu-id="7aff5-243">The media can be defined as a DVD drive (for example, D:\Sources\Sxs), or to a network share that the media files have been copied (for example, \\fileserver\windows2012\sources\Sxs).</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7aff5-244">Confira também</span><span class="sxs-lookup"><span data-stu-id="7aff5-244">See Also</span></span>


[<span data-ttu-id="7aff5-245">Requisitos de IIS para pools Front-End pools e servidores Standard Edition no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7aff5-245">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-iis-requirements-for-front-end-pools-and-standard-edition-servers.md)  
  

<span data-ttu-id="7aff5-246"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7aff5-246"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

