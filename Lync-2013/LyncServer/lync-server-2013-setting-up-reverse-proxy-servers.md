---
title: 'Lync Server 2013: Configurando servidores de proxy reverso'
description: 'Lync Server 2013: Configurando servidores proxy reverso.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up reverse proxy servers
ms:assetid: 00bc138a-243f-4389-bfa5-9c62fcc95132
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398069(v=OCS.15)
ms:contentKeyID: 48183225
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f8cd5842e4d735637406f6d0fa4f467f1cb8ed03
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390271"
---
# <a name="setting-up-reverse-proxy-servers-for-lync-server-2013"></a><span data-ttu-id="0c26d-103">Configurando servidores de proxy reverso para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c26d-103">Setting up reverse proxy servers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0c26d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0c26d-104">

<span> </span></span></span>

<span data-ttu-id="0c26d-105">_**Tópico da última modificação:** 2014-05-08_</span><span class="sxs-lookup"><span data-stu-id="0c26d-105">_**Topic Last Modified:** 2014-05-08_</span></span>

<span data-ttu-id="0c26d-106">Para implantações do Microsoft Lync Server 2013 Edge Server, um proxy reverso HTTPS na rede de perímetro é necessário para clientes externos acessarem os serviços da Web do Lync Server 2013 (chamados de *componentes da Web* no Office Communications Server) no diretor e no pool de casa do usuário.</span><span class="sxs-lookup"><span data-stu-id="0c26d-106">For Microsoft Lync Server 2013 Edge Server deployments, an HTTPS reverse proxy in the perimeter network is required for external clients to access the Lync Server 2013 Web Services (called *Web Components* in Office Communications Server) on the Director and the user’s home pool.</span></span> <span data-ttu-id="0c26d-107">Alguns dos recursos que exigem acesso externo por meio de um proxy reverso incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0c26d-107">Some of the features that require external access through a reverse proxy include the following:</span></span>

  - <span data-ttu-id="0c26d-108">Permitir que usuários externos Baixem o conteúdo da reunião para suas reuniões.</span><span class="sxs-lookup"><span data-stu-id="0c26d-108">Enabling external users to download meeting content for your meetings.</span></span>

  - <span data-ttu-id="0c26d-109">Permitir que usuários externos expandam grupos de distribuição.</span><span class="sxs-lookup"><span data-stu-id="0c26d-109">Enabling external users to expand distribution groups.</span></span>

  - <span data-ttu-id="0c26d-110">Permitir que usuários remotos baixem arquivos do serviço de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="0c26d-110">Enabling remote users to download files from the Address Book service.</span></span>

  - <span data-ttu-id="0c26d-111">Acessando o cliente Lync Web App.</span><span class="sxs-lookup"><span data-stu-id="0c26d-111">Accessing the Lync Web App client.</span></span>

  - <span data-ttu-id="0c26d-112">Acessando a página de configurações de conferência discada.</span><span class="sxs-lookup"><span data-stu-id="0c26d-112">Accessing the Dial-in Conferencing Settings webpage.</span></span>

  - <span data-ttu-id="0c26d-113">Habilitando dispositivos externos para se conectar ao serviço Web de atualização de dispositivos e obter atualizações.</span><span class="sxs-lookup"><span data-stu-id="0c26d-113">Enabling external devices to connect to Device Update web service and obtain updates.</span></span>

  - <span data-ttu-id="0c26d-114">Permitir que aplicativos móveis descubram e usem automaticamente as URLs de mobilidade (MCX) da Internet.</span><span class="sxs-lookup"><span data-stu-id="0c26d-114">Enabling mobile applications to automatically discover and use the mobility (Mcx) URLs from the Internet.</span></span>

  - <span data-ttu-id="0c26d-115">Habilitando o cliente do Lync 2013, o aplicativo Lync da Windows Store e o cliente móvel do Lync 2013 para localizar as URLs de descoberta do Lync (descoberta automática) e usar a API da Web de comunicação unificada (UCWA).</span><span class="sxs-lookup"><span data-stu-id="0c26d-115">Enabling the Lync 2013 client, Lync Windows Store app and Lync 2013 Mobile client to locate the Lync Discover (autodiscover) URLs and use Unified Communications Web API (UCWA).</span></span>

<span data-ttu-id="0c26d-116">Recomendamos que você configure seu proxy reverso HTTP para publicar todos os serviços Web em todos os pools.</span><span class="sxs-lookup"><span data-stu-id="0c26d-116">We recommend that you configure your HTTP reverse proxy to publish all Web Services in all pools.</span></span> <span data-ttu-id="0c26d-117">Publishing https://ExternalFQDN/ \* publica todos os diretórios virtuais do IIS para um pool.</span><span class="sxs-lookup"><span data-stu-id="0c26d-117">Publishing https:// ExternalFQDN/\* publishes all IIS virtual directories for a pool.</span></span> <span data-ttu-id="0c26d-118">Você precisa de uma regra de publicação para cada servidor Standard Edition, o pool de front-end ou o diretor ou o pool do diretor da sua organização.</span><span class="sxs-lookup"><span data-stu-id="0c26d-118">You need one publishing rule for each Standard Edition server, Front End pool, or Director or Director pool in your organization.</span></span>

<span data-ttu-id="0c26d-119">Além disso, você precisa publicar as URLs simples.</span><span class="sxs-lookup"><span data-stu-id="0c26d-119">In addition, you need to publish the simple URLs.</span></span> <span data-ttu-id="0c26d-120">Se a organização tiver um director ou um pool de directors, o proxy reverso HTTP escutará solicitações HTTP/HTTPS para URLs simples e os proxies para o diretório virtual de serviços Web externos no director ou no pool do diretor.</span><span class="sxs-lookup"><span data-stu-id="0c26d-120">If the organization has a Director or Director pool, the HTTP reverse proxy listens for HTTP/HTTPS requests to the simple URLs and proxies them to the external Web Services virtual directory on the Director or Director pool.</span></span> <span data-ttu-id="0c26d-121">Se você não implantou um director, será necessário designar um pool para manipular as solicitações para as URLs simples.</span><span class="sxs-lookup"><span data-stu-id="0c26d-121">If you have not deployed a Director, you need to designate one pool to handle requests to the simple URLs.</span></span> <span data-ttu-id="0c26d-122">(Se esse não for o pool inicial do usuário, ele será redirecionado para os serviços Web no pool primário do usuário).</span><span class="sxs-lookup"><span data-stu-id="0c26d-122">(If this is not the user’s home pool, it will redirect them onward to the Web Services on the user’s home pool).</span></span> <span data-ttu-id="0c26d-123">As URLs simples podem ser manipuladas por uma regra de publicação da Web dedicada ou você pode adicioná-la aos nomes públicos da regra de publicação na Web do diretor.</span><span class="sxs-lookup"><span data-stu-id="0c26d-123">The simple URLs can be handled by a dedicated web publishing rule, or you can add it to the public names of the web publishing rule for the Director.</span></span> <span data-ttu-id="0c26d-124">Você também precisa publicar a URL do serviço de descoberta automática externa.</span><span class="sxs-lookup"><span data-stu-id="0c26d-124">You also need to publish the external Autodiscover Service URL.</span></span>

<span data-ttu-id="0c26d-125">Você pode usar o Microsoft Forefront Threat Management Gateway 2010, o Microsoft Internet Security and Acceleration (ISA) Server 2006 SP1 ou o Internet Information Server 7,0, 7,5 ou 8,0 com o roteamento de solicitação de aplicativo (IIS ARR) como um proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="0c26d-125">You can use Microsoft Forefront Threat Management Gateway 2010, Microsoft Internet Security and Acceleration (ISA) Server 2006 SP1, or Internet Information Server 7.0, 7.5 or 8.0 with Application Request Routing (IIS ARR) as a reverse proxy.</span></span> <span data-ttu-id="0c26d-126">As etapas detalhadas desta seção descrevem como configurar o Forefront Threat Management Gateway 2010, e as etapas para configurar o ISA Server 2006 são quase idênticas.</span><span class="sxs-lookup"><span data-stu-id="0c26d-126">The detailed steps in this section describe how to configure Forefront Threat Management Gateway 2010, and the steps for configuring ISA Server 2006 are almost identical.</span></span> <span data-ttu-id="0c26d-127">Também é oferecida uma orientação para o IIS ARR.</span><span class="sxs-lookup"><span data-stu-id="0c26d-127">Guidance is also provided for IIS ARR.</span></span> <span data-ttu-id="0c26d-128">Se você estiver usando um proxy reverso diferente, consulte a documentação desse produto e mapeie os requisitos definidos aqui para os recursos associados em outros proxies reverso.</span><span class="sxs-lookup"><span data-stu-id="0c26d-128">If you are using a different reverse proxy, consult the documentation for that product and map the requirements defined here to the associated features in other reverse proxies.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="0c26d-129">Roteamento de solicitação de aplicativo do Internet Information Server (IIS ARR) é uma opção totalmente testada e com suporte para implementar um proxy reverso para o Lync Server 2010 e o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0c26d-129">Internet Information Server Application Request Routing (IIS ARR) is a fully tested and supported option for implementing a reverse proxy for Lync Server 2010 and Lync Server 2013.</span></span> <span data-ttu-id="0c26d-130">Em novembro de 2012, a Microsoft parou as vendas de licenças do ForeFront Threat Management Gateway 2010 ou da TMG.</span><span class="sxs-lookup"><span data-stu-id="0c26d-130">In November, 2012, Microsoft ceased license sales of ForeFront Threat Management Gateway 2010, or TMG.</span></span> <span data-ttu-id="0c26d-131">A TMG ainda é um produto totalmente compatível e ainda está disponível para venda em aparelhos vendidos por terceiros.</span><span class="sxs-lookup"><span data-stu-id="0c26d-131">TMG is still a fully supported product, and is still available for sale on appliances sold by third parties.</span></span> <span data-ttu-id="0c26d-132">Além disso, vários balanceadores de carga de hardware e firewalls de terceiros fornecem suporte de proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="0c26d-132">Also, many third party hardware load balancers and firewalls provide reverse proxy support.</span></span> <span data-ttu-id="0c26d-133">Para os balanceadores de carga de hardware e os firewalls que fornecem recursos de proxy reverso, consulte o fornecedor para obter instruções específicas sobre como configurar o produto para fornecer suporte de proxy reverso ao Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0c26d-133">For hardware load balancers and firewalls that provide reverse proxy features, check with your vendor for specific instructions on how to configure their product to provide reverse proxy support for Lync Server.</span></span> <span data-ttu-id="0c26d-134">Você também pode ver terceiros que enviaram documentação de seus produtos para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0c26d-134">You can also view third parties that have submitted documentation for their product to Microsoft.</span></span> <span data-ttu-id="0c26d-135">O suporte é fornecido por terceiros para sua solução.</span><span class="sxs-lookup"><span data-stu-id="0c26d-135">Support is provided by the third party for their solution.</span></span> <span data-ttu-id="0c26d-136">Para ver terceiros ativos no fornecimento de soluções, consulte <A href="https://go.microsoft.com/fwlink/?linkid=268730">infraestrutura qualificada para Microsoft Lync</A>.</span><span class="sxs-lookup"><span data-stu-id="0c26d-136">To see third parties that are active in providing solutions, see <A href="https://go.microsoft.com/fwlink/?linkid=268730">Infrastructure qualified for Microsoft Lync</A>.</span></span>



</div>

<span data-ttu-id="0c26d-137">Os tópicos e procedimentos a seguir usam o Forefront Threat Management Gateway 2010 e o IIS ARR como base para os procedimentos de implantação e configuração.</span><span class="sxs-lookup"><span data-stu-id="0c26d-137">The following topics and procedures use Forefront Threat Management Gateway 2010 and IIS ARR as the basis for the deployment and configuration procedures.</span></span>

  - [<span data-ttu-id="0c26d-138">Configurar FQDNs da web farm para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c26d-138">Configure web farm FQDNs for Lync Server 2013</span></span>](lync-server-2013-configure-web-farm-fqdns.md)

  - [<span data-ttu-id="0c26d-139">Configurar adaptadores de rede no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c26d-139">Configure network adapters in Lync Server 2013</span></span>](lync-server-2013-configure-network-adapters.md)

  - [<span data-ttu-id="0c26d-140">Solicitar e configurar um certificado para seu proxy HTTP reverso no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c26d-140">Request and configure a certificate for your reverse HTTP proxy in Lync Server 2013</span></span>](lync-server-2013-request-and-configure-a-certificate-for-your-reverse-http-proxy.md)

  - [<span data-ttu-id="0c26d-141">Configurar regras de publicação na Web para um único pool interno no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c26d-141">Configure web publishing rules for a single internal pool in Lync Server 2013</span></span>](lync-server-2013-configure-web-publishing-rules-for-a-single-internal-pool.md)

  - [<span data-ttu-id="0c26d-142">Verificar ou configurar autenticação e certificação nos diretórios virtuais de IIS no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c26d-142">Verify or configure authentication and certification on IIS virtual directories in Lync Server 2013</span></span>](lync-server-2013-verify-or-configure-authentication-and-certification-on-iis-virtual-directories.md)

  - [<span data-ttu-id="0c26d-143">Criar registros de DNS para servidores de proxy reverso no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c26d-143">Create DNS records for reverse proxy servers in Lync Server 2013</span></span>](lync-server-2013-create-dns-records-for-reverse-proxy-servers.md)

  - [<span data-ttu-id="0c26d-144">Verificar acesso por meio de seu proxy reverso no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c26d-144">Verify access through your reverse proxy in Lync Server 2013</span></span>](lync-server-2013-verify-access-through-your-reverse-proxy.md)

<div>

## <a name="before-you-begin"></a><span data-ttu-id="0c26d-145">Antes de começar</span><span class="sxs-lookup"><span data-stu-id="0c26d-145">Before You Begin</span></span>

<span data-ttu-id="0c26d-146">Para implantar com êxito o 2010 do Forefront Threat Management Gateway como seu proxy reverso, você precisa configurar e configurar um servidor, usando os pré-requisitos e requisitos de hardware definidos na documentação do Forefront Threat Management Gateway 2010.</span><span class="sxs-lookup"><span data-stu-id="0c26d-146">To successfully deploy Forefront Threat Management Gateway 2010 as your reverse proxy, you need to setup and configure a server, using the prerequisites and hardware requirements defined in the Forefront Threat Management Gateway 2010 documentation.</span></span> <span data-ttu-id="0c26d-147">Consulte o conjunto de tópicos a seguir para configurar corretamente o hardware e instalar o 2010 do Forefront Threat Management Gateway no servidor antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="0c26d-147">See the following topic set to properly configure the hardware and to install Forefront Threat Management Gateway 2010 on the server before proceeding.</span></span>

  - <span></span>  
    [<span data-ttu-id="0c26d-148">Forefront Threat Management Gateway (TMG) 2010</span><span class="sxs-lookup"><span data-stu-id="0c26d-148">Forefront Threat Management Gateway (TMG) 2010</span></span>](https://go.microsoft.com/fwlink/?linkid=291292)

  - <span></span>  
    [<span data-ttu-id="0c26d-149">Recomendações de hardware do Forefront TMG 2010</span><span class="sxs-lookup"><span data-stu-id="0c26d-149">Forefront TMG 2010 hardware recommendations</span></span>](https://go.microsoft.com/fwlink/?linkid=291293)

<span data-ttu-id="0c26d-150">Para implantar com êxito o ARR do IIS como seu proxy reverso, examine os tópicos a seguir para configurar o hardware e o software de pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="0c26d-150">To successfully deploy IIS ARR as your reverse proxy, review the following topics to configure the hardware and the prerequisite software.</span></span>

  - <span></span>  
    <span data-ttu-id="0c26d-151">Para instalar o IIS no Windows Server 2008 ou no Windows Server 2008 R2, confira [instalando o IIS 7 no Windows server 2008 ou Windows server 2008 R2](https://go.microsoft.com/fwlink/?linkid=291296)</span><span class="sxs-lookup"><span data-stu-id="0c26d-151">To install IIS on Windows Server 2008 or Windows Server 2008 R2, see [Installing IIS 7 on Windows Server 2008 or Windows Server 2008 R2](https://go.microsoft.com/fwlink/?linkid=291296)</span></span>

  - <span></span>  
    <span data-ttu-id="0c26d-152">Para instalar o IIS no Windows Server 2012, confira [instalando o IIS 8 no Windows server 2012](https://go.microsoft.com/fwlink/?linkid=291297)</span><span class="sxs-lookup"><span data-stu-id="0c26d-152">To install IIS on Windows Server 2012, see [Installing IIS 8 on Windows Server 2012](https://go.microsoft.com/fwlink/?linkid=291297)</span></span>

  - <span></span>  
    <span data-ttu-id="0c26d-153">Para instalar o IIS no Windows Server 2012 R2, confira [instalando o iis 8,5 no Windows server 2012 R2](https://go.microsoft.com/fwlink/?linkid=330687)</span><span class="sxs-lookup"><span data-stu-id="0c26d-153">To install IIS on Windows Server 2012 R2, see [Installing IIS 8.5 on Windows Server 2012 R2](https://go.microsoft.com/fwlink/?linkid=330687)</span></span>

  - <span></span>  
    <span data-ttu-id="0c26d-154">Para baixar a extensão de roteamento de solicitação do aplicativo para o IIS, siga as instruções em [solicitação do aplicativo roteamento v 2.5 Download](https://go.microsoft.com/fwlink/?linkid=291298)</span><span class="sxs-lookup"><span data-stu-id="0c26d-154">To download the Application Request Routing extension for IIS, follow the instructions at [Application Request Routing v2.5 Download](https://go.microsoft.com/fwlink/?linkid=291298)</span></span>

  - <span></span>  
    <span data-ttu-id="0c26d-155">Para instalar o ARR, para as instruções no [artigo instalar o roteamento de solicitação de aplicativo versão 2](https://go.microsoft.com/fwlink/?linkid=291299)</span><span class="sxs-lookup"><span data-stu-id="0c26d-155">To install ARR, for the instructions at [Install Application Request Routing Version 2](https://go.microsoft.com/fwlink/?linkid=291299)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0c26d-156">As instruções publicadas atualmente são para o ARR 2,0.</span><span class="sxs-lookup"><span data-stu-id="0c26d-156">The instructions currently posted are for ARR 2.0.</span></span> <span data-ttu-id="0c26d-157">Para a instalação da extensão, não há diferença entre as duas versões.</span><span class="sxs-lookup"><span data-stu-id="0c26d-157">For installation of the extension, there is no difference between the two versions.</span></span>

    
    <span data-ttu-id="0c26d-158"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0c26d-158"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

