---
title: 'Lync Server 2013: Requisitos adicionais de software'
description: 'Lync Server 2013: mais requisitos de software.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Additional software requirements
ms:assetid: 87b318e3-03ae-41f7-af5e-29bb294f6af0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398686(v=OCS.15)
ms:contentKeyID: 48184731
ms.date: 12/09/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbc36f23a2246c9d653e47954064182c756f0dff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443150"
---
# <a name="additional-software-requirements-for-lync-server-2013"></a><span data-ttu-id="a3628-103">Requisitos adicionais de software para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3628-103">Additional software requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3628-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3628-104">

<span> </span></span></span>

<span data-ttu-id="a3628-105">_**Tópico da última modificação:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="a3628-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="a3628-106">Além dos requisitos de hardware e sistema operacional das plataformas do servidor, o Lync Server 2013 requer a instalação de software adicional nos servidores que você implantar.</span><span class="sxs-lookup"><span data-stu-id="a3628-106">In addition to the hardware and operating system requirements for server platforms, Lync Server 2013 requires the installation of additional software on the servers that you deploy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a3628-107">Para obter detalhes sobre os requisitos da plataforma para servidores que executam o Lync Server, consulte <A href="lync-server-2013-server-hardware-platforms.md">plataformas de hardware do servidor para o Lync server 2013</A> e <A href="lync-server-2013-server-and-tools-operating-system-support.md">servidor e ferramentas, suporte ao sistema operacional do Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a3628-107">For details about the platform requirements for servers running Lync Server, see <A href="lync-server-2013-server-hardware-platforms.md">Server hardware platforms for Lync Server 2013</A> and <A href="lync-server-2013-server-and-tools-operating-system-support.md">Server and tools operating system support in Lync Server 2013</A>.</span></span> <span data-ttu-id="a3628-108">Para obter detalhes sobre os requisitos do sistema para computadores e dispositivos cliente, consulte <A href="lync-server-2013-planning-for-clients-and-devices.md">planejando para clientes e dispositivos no Lync Server 2013</A> na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="a3628-108">For details about system requirements for client computers and devices, see <A href="lync-server-2013-planning-for-clients-and-devices.md">Planning for clients and devices in Lync Server 2013</A> in the Planning documentation.</span></span> <span data-ttu-id="a3628-109">Para obter detalhes sobre os requisitos de software para ferramentas administrativas, consulte <A href="lync-server-2013-administrative-tools-software-requirements.md">requisitos de software para ferramentas administrativas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a3628-109">For details about software requirements for administrative tools, see <A href="lync-server-2013-administrative-tools-software-requirements.md">Administrative tools software requirements in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="additional-software-necessary-for-all-internal-server-roles"></a><span data-ttu-id="a3628-110">Software adicional necessário para todas as funções de servidor interno</span><span class="sxs-lookup"><span data-stu-id="a3628-110">Additional Software Necessary for All Internal Server Roles</span></span>

<span data-ttu-id="a3628-111">Esta seção lista o software necessário em todas as funções de servidor interno, que são todas as funções de servidor do Lync Server, exceto para o servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="a3628-111">This section lists software necessary on all internal server roles, which are all Lync Server server roles except for Edge Server.</span></span> <span data-ttu-id="a3628-112">Os requisitos para os servidores de borda e os pools de bordas são listados mais adiante neste tópico em **software adicional para servidores de borda**.</span><span class="sxs-lookup"><span data-stu-id="a3628-112">The requirements for the Edge Servers and Edge pools are listed later in this topic under **Additional Software for Edge Servers**.</span></span>

</div>

<div>

## <a name="windows-powershell-30"></a><span data-ttu-id="a3628-113">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="a3628-113">Windows PowerShell 3.0</span></span>

<span data-ttu-id="a3628-114">Cada servidor executando o Lync Server 2013 deve ter a versão correta do Windows PowerShell 3,0 instalada.</span><span class="sxs-lookup"><span data-stu-id="a3628-114">Each server running Lync Server 2013 must have the correct release of Windows PowerShell 3.0 installed.</span></span> <span data-ttu-id="a3628-115">Para obter detalhes, consulte [instalando o Windows PowerShell 3,0 para Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="a3628-115">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span></span>

</div>

<div>

## <a name="microsoft-net-framework-45"></a><span data-ttu-id="a3628-116">Microsoft.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="a3628-116">Microsoft .NET Framework 4.5</span></span>

<span data-ttu-id="a3628-117">O Lync Server requer o Microsoft .NET Framework 4,5 em todas as funções de servidor interno e em qualquer computador no qual você executará as ferramentas administrativas do Lync Server ou o Microsoft Lync Server 2013, ferramenta de planejamento.</span><span class="sxs-lookup"><span data-stu-id="a3628-117">Lync Server requires Microsoft .NET Framework 4.5 on all internal server roles and on any computer where you will run the Lync Server administrative tools or Microsoft Lync Server 2013, Planning Tool.</span></span> <span data-ttu-id="a3628-118">Para o Lync Server 2013, você deve instalar manualmente a edição de 64 bits do Microsoft .NET Framework 4,5 no servidor antes de instalar o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a3628-118">For Lync Server 2013, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span> <span data-ttu-id="a3628-119">Para instalá-lo manualmente, baixe a estrutura do Microsoft .NET 4,5 a partir do centro de download da Microsoft em [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span><span class="sxs-lookup"><span data-stu-id="a3628-119">To manually install it, download the Microsoft .NET 4.5 Framework from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span></span>

<div>

## <a name="installing-microsoft-net-framework-45-on-servers-running-windows-server-2012"></a><span data-ttu-id="a3628-120">Instalando o Microsoft .NET Framework 4,5 em servidores que executam o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3628-120">Installing Microsoft .NET Framework 4.5 on Servers Running Windows Server 2012</span></span>

<span data-ttu-id="a3628-121">Ao instalar o Microsoft .NET Framework 4,5 em servidores que executarão o Lync Server 2013 e o Windows Server 2012, você deve executar uma etapa adicional.</span><span class="sxs-lookup"><span data-stu-id="a3628-121">When you install Microsoft .NET Framework 4.5 on servers that will run Lync Server 2013 and Windows Server 2012, you must perform one additional step.</span></span> <span data-ttu-id="a3628-122">Após instalar o .NET Framework 4,5, use o Gerenciador de servidores para instalar a ativação HTTP.</span><span class="sxs-lookup"><span data-stu-id="a3628-122">After .NET Framework 4.5 is installed, use Server Manager to install HTTP Activation.</span></span>

<span data-ttu-id="a3628-123">**Para instalar a ativação HTTP do .NET 4,5 no Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a3628-123">**To Install .NET 4.5 HTTP Activation on Windows Server 2012**</span></span>

1.  <span data-ttu-id="a3628-124">No menu **Iniciar** , clique em **programas** e, em seguida, clique em **Ferramentas administrativas** e, em seguida, clique em **Gerenciador de servidores**.</span><span class="sxs-lookup"><span data-stu-id="a3628-124">From the **Start** menu, click **Programs**, then click **Administrative Tools**, then click **Server Manager**.</span></span>

2.  <span data-ttu-id="a3628-125">No Gerenciador de servidores, em **Resumo de recursos**, escolha **Adicionar recursos**.</span><span class="sxs-lookup"><span data-stu-id="a3628-125">In Server Manager, under **Features Summary**, choose **Add Features**.</span></span>

3.  <span data-ttu-id="a3628-126">Expanda o **.NET Framework 4,5**.</span><span class="sxs-lookup"><span data-stu-id="a3628-126">Expand **.NET Framework 4.5**.</span></span>

4.  <span data-ttu-id="a3628-127">Selecione **ativação do WCF** , se ainda não estiver selecionado.</span><span class="sxs-lookup"><span data-stu-id="a3628-127">Select **WCF Activation** if it isn’t already selected.</span></span> <span data-ttu-id="a3628-128">Em seguida, selecione **ativação http**.</span><span class="sxs-lookup"><span data-stu-id="a3628-128">Then select **HTTP Activation**.</span></span>

5.  <span data-ttu-id="a3628-129">Clique em **Avançar** e siga as instruções para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="a3628-129">Click **Next** and follow the prompts to finish the installation.</span></span>

</div>

</div>

<div>

## <a name="windows-identity-foundation"></a><span data-ttu-id="a3628-130">Windows Identity Foundation</span><span class="sxs-lookup"><span data-stu-id="a3628-130">Windows Identity Foundation</span></span>

<span data-ttu-id="a3628-131">A **base de identidade do Windows** no Lync Server 2013 requer a instalação do Windows Identity Foundation para dar suporte a cenários de autenticação do servidor para o servidor.</span><span class="sxs-lookup"><span data-stu-id="a3628-131">**Windows Identity Foundation** in Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server to server authentication scenarios.</span></span> <span data-ttu-id="a3628-132">O Windows Server 2008 R2 e o Windows Server 2012 exigem procedimentos diferentes para instalar a base de identidades do Windows.</span><span class="sxs-lookup"><span data-stu-id="a3628-132">Windows Server 2008 R2 and Windows Server 2012 require different procedures to install the Windows Identify Foundation.</span></span> <span data-ttu-id="a3628-133">Selecione o sistema operacional do seu servidor na lista a seguir:</span><span class="sxs-lookup"><span data-stu-id="a3628-133">Select your server operating system from the following list:</span></span>

  - <span data-ttu-id="a3628-134">Windows Server 2008 R2 para Windows Server 2008 R2, você verifica se ele já foi instalado em seu computador.</span><span class="sxs-lookup"><span data-stu-id="a3628-134">Windows Server 2008 R2   For Windows Server 2008 R2, you check to see if it has already been installed on your computer.</span></span> <span data-ttu-id="a3628-135">Para fazer isso, vá para **Adicionar/remover programas**, **Exibir atualizações instaladas** e procurar em **Windows** para a entrada do **Windows Identity Foundation (KB974405)**.</span><span class="sxs-lookup"><span data-stu-id="a3628-135">To do this, go to **Add/Remove Programs**, **View Installed Updates**, and look under **Windows** for the entry **Windows Identity Foundation (KB974405)**.</span></span> <span data-ttu-id="a3628-136">Para obter detalhes sobre como instalar o Windows Identity Foundation, consulte [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) .</span><span class="sxs-lookup"><span data-stu-id="a3628-136">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>

  - <span data-ttu-id="a3628-137">Windows Server 2012 para Windows Server 2012, você usa o **Gerenciador de servidores** para instalar o Windows Identity Foundation.</span><span class="sxs-lookup"><span data-stu-id="a3628-137">Windows Server 2012   For Windows Server 2012, you use **Server Manager** to install the Windows Identity Foundation.</span></span> <span data-ttu-id="a3628-138">No **Assistente Adicionar funções e recursos** do Gerenciador de servidores, selecione **recursos**.</span><span class="sxs-lookup"><span data-stu-id="a3628-138">In the Server Manager **Add Roles and Features Wizard**, select **Features**.</span></span> <span data-ttu-id="a3628-139">Selecione **Windows Identity Foundation 3,5** na lista.</span><span class="sxs-lookup"><span data-stu-id="a3628-139">Select **Windows Identity Foundation 3.5** from the list.</span></span> <span data-ttu-id="a3628-140">Clique em **Avançar** e, em seguida, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="a3628-140">Click **Next**, then click **Install**.</span></span>

</div>

<div>

## <a name="additional-software-for-all-front-end-servers-and-standard-edition-servers"></a><span data-ttu-id="a3628-141">Software adicional para todos os servidores front-end e servidores Standard Edition</span><span class="sxs-lookup"><span data-stu-id="a3628-141">Additional Software for All Front End Servers and Standard Edition Servers</span></span>

<span data-ttu-id="a3628-142">Todos os servidores de front-end e servidores Standard Edition também devem executar o IIS (serviços de informações da Internet) com determinados módulos.</span><span class="sxs-lookup"><span data-stu-id="a3628-142">All Front End Servers and Standard Edition servers must also run Internet Information Services (IIS) with certain modules.</span></span> <span data-ttu-id="a3628-143">Além disso, todos os servidores de front-end e servidores da edição padrão em que a conferência, chamadas de aplicativo, anúncio ou grupos de resposta são implementadas devem executar o tempo de execução do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="a3628-143">Additionally, all Front End Servers and Standard Edition servers where conferencing, Call Park application, Announcement, or Response Groups are deployed must run Windows Media Format Runtime.</span></span>

<div>

## <a name="internet-information-services-iis"></a><span data-ttu-id="a3628-144">IIS (Serviços de Informações da Internet)</span><span class="sxs-lookup"><span data-stu-id="a3628-144">Internet Information Services (IIS)</span></span>

<span data-ttu-id="a3628-145">Os servidores front-end e servidores Standard Edition devem executar o IIS (serviços de informações da Internet), com os seguintes módulos:</span><span class="sxs-lookup"><span data-stu-id="a3628-145">Front End Servers and Standard Edition servers must run Internet Information Services (IIS), with the following modules:</span></span>

  - <span data-ttu-id="a3628-146">Conteúdo estático</span><span class="sxs-lookup"><span data-stu-id="a3628-146">Static Content</span></span>

  - <span data-ttu-id="a3628-147">Documento padrão</span><span class="sxs-lookup"><span data-stu-id="a3628-147">Default Document</span></span>

  - <span data-ttu-id="a3628-148">Erros HTTP</span><span class="sxs-lookup"><span data-stu-id="a3628-148">HTTP Errors</span></span>

  - <span data-ttu-id="a3628-149">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="a3628-149">ASP.NET</span></span>

  - <span data-ttu-id="a3628-150">Extensibilidade .NET</span><span class="sxs-lookup"><span data-stu-id="a3628-150">.NET Extensibility</span></span>

  - <span data-ttu-id="a3628-151">Extensões da API de servidor da Internet (ISAPI)</span><span class="sxs-lookup"><span data-stu-id="a3628-151">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="a3628-152">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="a3628-152">ISAPI Filters</span></span>

  - <span data-ttu-id="a3628-153">Log HTTP</span><span class="sxs-lookup"><span data-stu-id="a3628-153">HTTP Logging</span></span>

  - <span data-ttu-id="a3628-154">Ferramentas de log</span><span class="sxs-lookup"><span data-stu-id="a3628-154">Logging Tools</span></span>

  - <span data-ttu-id="a3628-155">Rastreamento</span><span class="sxs-lookup"><span data-stu-id="a3628-155">Tracing</span></span>

  - <span data-ttu-id="a3628-156">Autenticação do Windows</span><span class="sxs-lookup"><span data-stu-id="a3628-156">Windows Authentication</span></span>

  - <span data-ttu-id="a3628-157">Requisição de filtro</span><span class="sxs-lookup"><span data-stu-id="a3628-157">Request Filtering</span></span>

  - <span data-ttu-id="a3628-158">Compressão de conteúdo estático</span><span class="sxs-lookup"><span data-stu-id="a3628-158">Static Content Compression</span></span>

  - <span data-ttu-id="a3628-159">Compactação de conteúdo dinâmico</span><span class="sxs-lookup"><span data-stu-id="a3628-159">Dynamic Content Compression</span></span>

  - <span data-ttu-id="a3628-160">Console de gerenciamento IIS</span><span class="sxs-lookup"><span data-stu-id="a3628-160">IIS Management Console</span></span>

  - <span data-ttu-id="a3628-161">Ferramentas e scripts de gerenciamento IIS</span><span class="sxs-lookup"><span data-stu-id="a3628-161">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="a3628-162">Autenticação anônima (instalada por padrão quando o IIS é instalado)</span><span class="sxs-lookup"><span data-stu-id="a3628-162">Anonymous Authentication (this is installed by default when IIS is installed.)</span></span>

  - <span data-ttu-id="a3628-163">Autenticação de mapeamento de certificado de cliente</span><span class="sxs-lookup"><span data-stu-id="a3628-163">Client Certificate Mapping Authentication</span></span>

</div>

<div>

## <a name="windows-media-format-runtime-and-windows-desktop-experience"></a><span data-ttu-id="a3628-164">Experiência em tempo de execução do Windows Media Format e área de trabalho do Windows</span><span class="sxs-lookup"><span data-stu-id="a3628-164">Windows Media Format Runtime and Windows Desktop Experience</span></span>

<span data-ttu-id="a3628-165">**Experiência da área de trabalho do Windows** Todos os servidores front-end e servidores Standard Edition em que a conferência será implantada devem ter o tempo de execução do Windows Media Format instalado, o que, com exceção do Windows Server 2012, é instalado como parte da experiência da área de trabalho do Windows.</span><span class="sxs-lookup"><span data-stu-id="a3628-165">**Windows Desktop Experience** All Front End Servers and Standard Edition servers where conferencing will be deployed must have the Windows Media Format Runtime installed, which, except for Windows Server 2012 is installed as part of the Windows desktop experience.</span></span> <span data-ttu-id="a3628-166">O Windows Server 2012 requer o Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a3628-166">Windows Server 2012 requires Microsoft Media Foundation.</span></span> <span data-ttu-id="a3628-167">O tempo de execução do Windows Media Format é necessário para executar os arquivos de áudio do Windows Media (. WMA) que os aplicativos de estacionamento de chamada, anúncio e resposta são reproduzidos para anúncios e músicas.</span><span class="sxs-lookup"><span data-stu-id="a3628-167">The Windows Media Format Runtime is required to run the Windows Media Audio (.wma) files that the Call Park, Announcement, and Response Group applications play for announcements and music.</span></span>

<span data-ttu-id="a3628-168">Recomendamos que você instale a experiência da área de trabalho do Windows antes de instalar o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a3628-168">We recommend that you install Windows desktop experience before you install Lync Server 2013.</span></span> <span data-ttu-id="a3628-169">Se o Lync Server 2013 não encontrar esse software no servidor, ele solicitará que você o instale e, em seguida, deverá reiniciar o servidor para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="a3628-169">If Lync Server 2013 does not find this software on the server, it will prompt you to install it, and then you must restart the server to complete installation.</span></span>

</div>

</div>

<div>

## <a name="additional-software-for-front-end-servers-and-standard-edition-servers-running-on-windows-server-2012"></a><span data-ttu-id="a3628-170">Software adicional para servidores front-end e servidores Standard Edition em execução no Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3628-170">Additional Software for Front End Servers and Standard Edition Servers Running on Windows Server 2012</span></span>

<span data-ttu-id="a3628-171">Os servidores front-end exigem o .NET 3,5, que não é instalado por padrão no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a3628-171">Front End Servers require .NET 3.5, which is not installed by default on Windows Server 2012.</span></span> <span data-ttu-id="a3628-172">Para instalá-lo, coloque a mídia de instalação do Windows Server 2012 na unidade D e digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a3628-172">To install it, put your Windows Server 2012 installation media in Drive D and type the following:</span></span>

    Add-WindowsFeature RSAT-ADDS, Web-Server, Web-Static-Content, Web-Default-Doc, Web-Http-Errors, Web-Asp-Net, Web-Net-Ext, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Logging, Web-Log-Libraries, Web-Request-Monitor, Web-Http-Tracing, Web-Basic-Auth, Web-Windows-Auth, Web-Client-Auth, Web-Filtering, Web-Stat-Compression, Web-Dyn-Compression, NET-WCF-HTTP-Activation45, Web-Asp-Net45, Web-Mgmt-Tools, Web-Scripting-Tools, Web-Mgmt-Compat, Desktop-Experience, Telnet-Client, BITS -Source D:\sources\sxs

<span data-ttu-id="a3628-173">Para obter detalhes sobre como instalar o .NET 3,5 em servidores que executam o Windows Server 2012, consulte "Microsoft .NET Framework 3,5 considerações de implantação" em <https://go.microsoft.com/fwlink/p/?linkid=275032> .</span><span class="sxs-lookup"><span data-stu-id="a3628-173">For details about installing .NET 3.5 on servers running Windows Server 2012, see "Microsoft .NET Framework 3.5 Deployment Considerations" at <https://go.microsoft.com/fwlink/p/?linkid=275032>.</span></span>

</div>

<div>

## <a name="additional-software-for-directors"></a><span data-ttu-id="a3628-174">Software adicional para directors</span><span class="sxs-lookup"><span data-stu-id="a3628-174">Additional Software for Directors</span></span>

<span data-ttu-id="a3628-175">Os diretores devem executar o IIS (serviços de informações da Internet), com os seguintes módulos:</span><span class="sxs-lookup"><span data-stu-id="a3628-175">Directors must run Internet Information Services (IIS), with the following modules:</span></span>

  - <span data-ttu-id="a3628-176">Conteúdo estático</span><span class="sxs-lookup"><span data-stu-id="a3628-176">Static Content</span></span>

  - <span data-ttu-id="a3628-177">Documento padrão</span><span class="sxs-lookup"><span data-stu-id="a3628-177">Default Document</span></span>

  - <span data-ttu-id="a3628-178">Erros HTTP</span><span class="sxs-lookup"><span data-stu-id="a3628-178">HTTP Errors</span></span>

  - <span data-ttu-id="a3628-179">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="a3628-179">ASP.NET</span></span>

  - <span data-ttu-id="a3628-180">Extensibilidade .NET</span><span class="sxs-lookup"><span data-stu-id="a3628-180">.NET Extensibility</span></span>

  - <span data-ttu-id="a3628-181">Extensões da API de servidor da Internet (ISAPI)</span><span class="sxs-lookup"><span data-stu-id="a3628-181">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="a3628-182">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="a3628-182">ISAPI Filters</span></span>

  - <span data-ttu-id="a3628-183">Log HTTP</span><span class="sxs-lookup"><span data-stu-id="a3628-183">HTTP Logging</span></span>

  - <span data-ttu-id="a3628-184">Ferramentas de log</span><span class="sxs-lookup"><span data-stu-id="a3628-184">Logging Tools</span></span>

  - <span data-ttu-id="a3628-185">Rastreamento</span><span class="sxs-lookup"><span data-stu-id="a3628-185">Tracing</span></span>

  - <span data-ttu-id="a3628-186">Autenticação do Windows</span><span class="sxs-lookup"><span data-stu-id="a3628-186">Windows Authentication</span></span>

  - <span data-ttu-id="a3628-187">Requisição de filtro</span><span class="sxs-lookup"><span data-stu-id="a3628-187">Request Filtering</span></span>

  - <span data-ttu-id="a3628-188">Compressão de conteúdo estático</span><span class="sxs-lookup"><span data-stu-id="a3628-188">Static Content Compression</span></span>

  - <span data-ttu-id="a3628-189">Console de gerenciamento IIS</span><span class="sxs-lookup"><span data-stu-id="a3628-189">IIS Management Console</span></span>

  - <span data-ttu-id="a3628-190">Ferramentas e scripts de gerenciamento IIS</span><span class="sxs-lookup"><span data-stu-id="a3628-190">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="a3628-191">Autenticação anônima (instalada por padrão quando o IIS é instalado)</span><span class="sxs-lookup"><span data-stu-id="a3628-191">Anonymous Authentication (This is installed by default when IIS is installed.)</span></span>

  - <span data-ttu-id="a3628-192">Autenticação de mapeamento de certificado de cliente</span><span class="sxs-lookup"><span data-stu-id="a3628-192">Client Certificate Mapping Authentication</span></span>

</div>

<div>

## <a name="additional-software-for-persistent-chat-front-end-servers"></a><span data-ttu-id="a3628-193">Software adicional para servidores de front-end de chat persistente</span><span class="sxs-lookup"><span data-stu-id="a3628-193">Additional Software for Persistent Chat Front End Servers</span></span>

<span data-ttu-id="a3628-194">Os servidores de front-end de chat persistente devem executar o enfileiramento de mensagens (também conhecido como MSMQ), que é um componente do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a3628-194">Persistent Chat Front End Servers must run Message Queuing (also known as MSMQ), which is a component of Windows Server.</span></span>

<span data-ttu-id="a3628-195">Para obter informações sobre como habilitar o MSMQ, [clique aqui.](https://technet.microsoft.com/library/cc771474.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3628-195">For information on enabling MSMQ, [click here.](https://technet.microsoft.com/library/cc771474.aspx)</span></span>

</div>

<div>

## <a name="additional-software-for-edge-servers"></a><span data-ttu-id="a3628-196">Software adicional para servidores Edge</span><span class="sxs-lookup"><span data-stu-id="a3628-196">Additional Software for Edge Servers</span></span>

<span data-ttu-id="a3628-197">Os servidores de borda exigem o seguinte software:</span><span class="sxs-lookup"><span data-stu-id="a3628-197">Edge Servers require the following software:</span></span>

  - <span data-ttu-id="a3628-198">Cada servidor executando o Lync Server 2013 deve ter a versão correta do Windows PowerShell 3,0 instalada.</span><span class="sxs-lookup"><span data-stu-id="a3628-198">Each server running Lync Server 2013 must have the correct release of Windows PowerShell 3.0 installed.</span></span> <span data-ttu-id="a3628-199">Para obter detalhes, consulte [instalando o Windows PowerShell 3,0 para Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="a3628-199">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span></span>

  - <span data-ttu-id="a3628-200">O Lync Server requer o Microsoft .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="a3628-200">Lync Server requires Microsoft .NET Framework 4.5.</span></span> <span data-ttu-id="a3628-201">Para o Lync Server 2013 instalado no Windows Server 2008 R2, você deve instalar manualmente a edição de 64 bits do Microsoft .NET Framework 4,5 no servidor antes de instalar o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a3628-201">For Lync Server 2013 installed on Windows Server 2008 R2, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span> <span data-ttu-id="a3628-202">Para instalá-lo manualmente, baixe a estrutura do Microsoft .NET 4,5 a partir do centro de download da Microsoft em [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span><span class="sxs-lookup"><span data-stu-id="a3628-202">To manually install it, download the Microsoft .NET 4.5 Framework from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span></span>

  - <span data-ttu-id="a3628-203">A **base de identidade do Windows** no Lync Server 2013 requer a instalação do Windows Identity Foundation para dar suporte a cenários de autenticação do servidor para o servidor.</span><span class="sxs-lookup"><span data-stu-id="a3628-203">**Windows Identity Foundation** in Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server to server authentication scenarios.</span></span> <span data-ttu-id="a3628-204">O Windows Server 2008 R2 e o Windows Server 2012 exigem procedimentos diferentes para instalar a base de identidades do Windows.</span><span class="sxs-lookup"><span data-stu-id="a3628-204">Windows Server 2008 R2 and Windows Server 2012 require different procedures to install the Windows Identify Foundation.</span></span> <span data-ttu-id="a3628-205">Selecione o sistema operacional do seu servidor na lista a seguir:</span><span class="sxs-lookup"><span data-stu-id="a3628-205">Select your server operating system from the following list:</span></span>
    
      - <span data-ttu-id="a3628-206">Windows Server 2008 R2 para Windows Server 2008 R2, você verifica se ele já foi instalado em seu computador.</span><span class="sxs-lookup"><span data-stu-id="a3628-206">Windows Server 2008 R2   For Windows Server 2008 R2, you check to see if it has already been installed on your computer.</span></span> <span data-ttu-id="a3628-207">Para fazer isso, vá para **Adicionar/remover programas**, **Exibir atualizações instaladas** e procurar em **Windows** para a entrada do **Windows Identity Foundation (KB974405)**.</span><span class="sxs-lookup"><span data-stu-id="a3628-207">To do this, go to **Add/Remove Programs**, **View Installed Updates**, and look under **Windows** for the entry **Windows Identity Foundation (KB974405)**.</span></span> <span data-ttu-id="a3628-208">Para obter detalhes sobre como instalar o Windows Identity Foundation, consulte [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) .</span><span class="sxs-lookup"><span data-stu-id="a3628-208">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>
    
      - <span data-ttu-id="a3628-209">Windows Server 2012 para Windows Server 2012, você usa o **Gerenciador de servidores** para instalar o Windows Identity Foundation.</span><span class="sxs-lookup"><span data-stu-id="a3628-209">Windows Server 2012   For Windows Server 2012, you use **Server Manager** to install the Windows Identity Foundation.</span></span> <span data-ttu-id="a3628-210">No **Assistente Adicionar funções e recursos** do Gerenciador de servidores, selecione **recursos**.</span><span class="sxs-lookup"><span data-stu-id="a3628-210">In the Server Manager **Add Roles and Features Wizard**, select **Features**.</span></span> <span data-ttu-id="a3628-211">Selecione **Windows Identity Foundation 3,5** na lista.</span><span class="sxs-lookup"><span data-stu-id="a3628-211">Select **Windows Identity Foundation 3.5** from the list.</span></span> <span data-ttu-id="a3628-212">Clique em **Avançar** e, em seguida, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="a3628-212">Click **Next**, then click **Install**.</span></span>

</div>

<div>

## <a name="do-not-install-layered-socket-providers-on-media-servers"></a><span data-ttu-id="a3628-213">Não instalar provedores de soquete em camadas em servidores de mídia</span><span class="sxs-lookup"><span data-stu-id="a3628-213">Do Not Install Layered Socket Providers on Media Servers</span></span>

<span data-ttu-id="a3628-214">Não instale qualquer software cliente do Microsoft Internet Security and Acceleration (ISA) Server ou qualquer outro software de provedores de serviços em camadas (LSP) Winsock em qualquer servidor front-end ou servidores autônomos de mediação.</span><span class="sxs-lookup"><span data-stu-id="a3628-214">Do not install any Microsoft Internet Security and Acceleration (ISA) Server client software, or any other Winsock Layered Service Providers (LSP) software, on any Front End Servers or stand-alone Mediation Servers.</span></span> <span data-ttu-id="a3628-215">A instalação deste software pode causar um desempenho de tráfego de mídia ruim.</span><span class="sxs-lookup"><span data-stu-id="a3628-215">Installing this software could cause poor media traffic performance.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a3628-216">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3628-216">See Also</span></span>


[<span data-ttu-id="a3628-217">Requisitos de software de ferramentas administrativas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3628-217">Administrative tools software requirements in Lync Server 2013</span></span>](lync-server-2013-administrative-tools-software-requirements.md)  
  

<span data-ttu-id="a3628-218"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3628-218"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

