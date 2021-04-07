---
title: 'Lync Server 2013: Planejamento para implantações híbridas'
description: 'Lync Server 2013: Planejamento para implantações híbridas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424545"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a><span data-ttu-id="04b6e-103">Planejamento para implantações híbridas do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="04b6e-103">Planning for Lync Server 2013 hybrid deployments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="04b6e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="04b6e-104">

<span> </span></span></span>

<span data-ttu-id="04b6e-105">_**Tópico Última Modificação:** 2016-05-25_</span><span class="sxs-lookup"><span data-stu-id="04b6e-105">_**Topic Last Modified:** 2016-05-25_</span></span>

<span data-ttu-id="04b6e-106">Você deve considerar os seguintes requisitos para usuários e sua infraestrutura de rede durante o planejamento de uma implantação híbrida.</span><span class="sxs-lookup"><span data-stu-id="04b6e-106">You should consider the following requirements for users and your network infrastructure while planning for a hybrid deployment.</span></span>

<div>

## <a name="infrastructure-requirements"></a><span data-ttu-id="04b6e-107">Requisitos de infraestrutura</span><span class="sxs-lookup"><span data-stu-id="04b6e-107">Infrastructure Requirements</span></span>

<span data-ttu-id="04b6e-108">Você deve ter o seguinte configurado em seu ambiente para implementar e implantar uma implantação híbrida.</span><span class="sxs-lookup"><span data-stu-id="04b6e-108">You must have the following configured in your environment in order to implement and deploy a hybrid deployment.</span></span>

  - <span data-ttu-id="04b6e-109">Uma organização do Microsoft 365 ou do Office 365 com o Skype for Business Online habilitado.</span><span class="sxs-lookup"><span data-stu-id="04b6e-109">A Microsoft 365 or Office 365 organization with Skype for Business Online enabled.</span></span> <span data-ttu-id="04b6e-110">Observe que você pode usar apenas um único locatário para uma configuração híbrida com sua implantação local.</span><span class="sxs-lookup"><span data-stu-id="04b6e-110">Note that you can use only a single tenant for a hybrid configuration with your on-premises deployment.</span></span>

  - <span data-ttu-id="04b6e-111">Uma única implantação local (infraestrutura) do Skype for Business Server ou do Lync Server implantado em uma topologia com suporte.</span><span class="sxs-lookup"><span data-stu-id="04b6e-111">A single on-premises deployment (infrastructure) of Skype for Business Server or Lync Server that is deployed in a supported topology.</span></span> <span data-ttu-id="04b6e-112">Consulte Requisitos de Topologia.</span><span class="sxs-lookup"><span data-stu-id="04b6e-112">See Topology Requirements.</span></span>
    
    <span data-ttu-id="04b6e-113">Para obter informações sobre como configurar sua implantação do Lync Server 2013 ou Lync Server 2010 para híbrido, consulte [Configuring Lync Server 2013 hybrid deployments](lync-server-2013-configuring-hybrid-deployments.md).</span><span class="sxs-lookup"><span data-stu-id="04b6e-113">For information about configuring your Lync Server 2013 or Lync Server 2010 deployment for hybrid, see [Configuring Lync Server 2013 hybrid deployments](lync-server-2013-configuring-hybrid-deployments.md).</span></span>

  - <span data-ttu-id="04b6e-114">Ferramentas administrativas do Skype for Business Server 2015.</span><span class="sxs-lookup"><span data-stu-id="04b6e-114">Skype for Business Server 2015 administrative tools.</span></span> <span data-ttu-id="04b6e-115">Se você estiver usando o Lync Server 2013 ou o Lync Server 2010, poderá usar as ferramentas administrativas do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04b6e-115">If you are using Lync Server 2013 or Lync Server 2010, you can use the Lync Server 2013 administrative tools.</span></span>

  - <span data-ttu-id="04b6e-116">Para dar suporte ao Logon Único com o Microsoft 365 ou o Office 365 para que os usuários possam usar as mesmas credenciais de logon para entrar no Office como fazem no local, você pode usar os recursos de sincronização de senha do Azure Active Directory (AAD) Connect.</span><span class="sxs-lookup"><span data-stu-id="04b6e-116">To support Single Sign-on with Microsoft 365 or Office 365 so that users can use the same login credentials for signing in to Office as they do on-premises, you can use the password sync features of Azure Active Directory (AAD) Connect.</span></span> <span data-ttu-id="04b6e-117">Você também pode usar os Serviços de Federação do Active Directory (AD FS) para um único login com o Microsoft 365 ou o Office 365.</span><span class="sxs-lookup"><span data-stu-id="04b6e-117">You can also use Active Directory Federation Services (AD FS) for single sign-on with Microsoft 365 or Office 365.</span></span>
    
    <span data-ttu-id="04b6e-118">Para obter mais informações, consulte Integrando suas identidades locais [com o Azure Active Directory](https://go.microsoft.com/fwlink/p/?linkid=619754).</span><span class="sxs-lookup"><span data-stu-id="04b6e-118">For more information, see [Integrating your on-premises identities with Azure Active Directory](https://go.microsoft.com/fwlink/p/?linkid=619754).</span></span>

  - <span data-ttu-id="04b6e-119">Uma solução de sincronização de diretório único para manter seus objetos Do Active Directory locais e online sincronizados.</span><span class="sxs-lookup"><span data-stu-id="04b6e-119">A single directory synchronization solution to keep your on-premises and online Active Directory objects synchronized.</span></span> <span data-ttu-id="04b6e-120">Para obter detalhes sobre a Sincronização de Diretórios, consulte [Ferramentas de Integração de Diretório.](https://go.microsoft.com/fwlink/p/?linkid=530320)</span><span class="sxs-lookup"><span data-stu-id="04b6e-120">For details about Directory Synchronization, see [Directory Integration Tools](https://go.microsoft.com/fwlink/p/?linkid=530320).</span></span>

</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="04b6e-121">Suporte ao cliente do Lync</span><span class="sxs-lookup"><span data-stu-id="04b6e-121">Lync Client Support</span></span>

<span data-ttu-id="04b6e-122">Há algumas diferenças nos recursos suportados nos clientes do Lync, bem como nos recursos disponíveis em ambientes locais e online.</span><span class="sxs-lookup"><span data-stu-id="04b6e-122">There are some differences in the features supported in Lync clients, as well as the features available in on-premises and online environments.</span></span> <span data-ttu-id="04b6e-123">Antes de decidir onde deseja a casa dos usuários em sua organização, você pode exibir o suporte ao cliente para as várias configurações do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="04b6e-123">Before you decide where you want to home users in your organization, you can view the client support for the various configurations of Lync Server.</span></span> <span data-ttu-id="04b6e-124">Os seguintes clientes têm suporte com o Skype for Business Online em uma implantação híbrida do Lync:</span><span class="sxs-lookup"><span data-stu-id="04b6e-124">The following clients are supported with Skype for Business Online in a Lync hybrid deployment:</span></span>

  - <span data-ttu-id="04b6e-125">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="04b6e-125">Lync 2010</span></span>

  - <span data-ttu-id="04b6e-126">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="04b6e-126">Lync 2013</span></span>

  - <span data-ttu-id="04b6e-127">Aplicativo Lync Windows Store</span><span class="sxs-lookup"><span data-stu-id="04b6e-127">Lync Windows Store app</span></span>

  - <span data-ttu-id="04b6e-128">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="04b6e-128">Lync Web App</span></span>

  - <span data-ttu-id="04b6e-129">Lync Mobile</span><span class="sxs-lookup"><span data-stu-id="04b6e-129">Lync Mobile</span></span>

  - <span data-ttu-id="04b6e-130">Lync para Mac 2011</span><span class="sxs-lookup"><span data-stu-id="04b6e-130">Lync for Mac 2011</span></span>

  - <span data-ttu-id="04b6e-131">Sistema de Salas do Lync</span><span class="sxs-lookup"><span data-stu-id="04b6e-131">Lync Room System</span></span>

  - <span data-ttu-id="04b6e-132">Lync Basic 2013</span><span class="sxs-lookup"><span data-stu-id="04b6e-132">Lync Basic 2013</span></span>

<span data-ttu-id="04b6e-133">Para obter detalhes sobre o suporte ao cliente, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="04b6e-133">For details about client support, see the following topics:</span></span>

  - [<span data-ttu-id="04b6e-134">Clientes do Lync Online</span><span class="sxs-lookup"><span data-stu-id="04b6e-134">Clients for Lync Online</span></span>](https://go.microsoft.com/fwlink/?linkid=281902)

  - [<span data-ttu-id="04b6e-135">Tabelas de comparação dos clientes para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="04b6e-135">Client comparison tables for Lync Server 2013</span></span>](lync-server-2013-desktop-client-comparison-tables.md)

  - [<span data-ttu-id="04b6e-136">Tabela de comparação de clientes móveis para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="04b6e-136">Mobile client comparison tables for Lync Server 2013</span></span>](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a><span data-ttu-id="04b6e-137">Requisitos de topologia</span><span class="sxs-lookup"><span data-stu-id="04b6e-137">Topology Requirements</span></span>

<span data-ttu-id="04b6e-138">Para configurar sua implantação híbrida com o Skype for Business Online, você precisa ter uma das seguintes topologias com suporte:</span><span class="sxs-lookup"><span data-stu-id="04b6e-138">To configure your deployment for hybrid with Skype for Business Online, you need to have one of the following supported topologies:</span></span>

  - <span data-ttu-id="04b6e-139">Uma implantação do Skype for Business Server 2015 com todos os servidores executando o Skype for Business Server 2015.</span><span class="sxs-lookup"><span data-stu-id="04b6e-139">A Skype for Business Server 2015 deployment with all servers running Skype for Business Server 2015.</span></span>

  - <span data-ttu-id="04b6e-140">Uma implantação do Lync Server 2013 com todos os servidores executando o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04b6e-140">A Lync Server 2013 deployment with all servers running Lync Server 2013.</span></span>

  - <span data-ttu-id="04b6e-141">Uma implantação do Lync Server 2010 com todos os servidores executando o Lync Server 2010 com as atualizações cumulativas mais recentes.</span><span class="sxs-lookup"><span data-stu-id="04b6e-141">A Lync Server 2010 deployment with all servers running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="04b6e-142">O Servidor de Borda de federação e o servidor de próximo salto do Servidor de Borda de federação devem estar executando o Lync Server 2010 com as atualizações cumulativas mais recentes.</span><span class="sxs-lookup"><span data-stu-id="04b6e-142">The federation Edge Server and next hop server from the federation Edge Server must be running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="04b6e-143">As Ferramentas Administrativas do Skype for Business Server 2015 ou Lync Server 2013 devem ser instaladas em pelo menos um servidor ou estação de trabalho de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="04b6e-143">The Skype for Business Server 2015 or Lync Server 2013 Administrative Tools must be installed on at least one server or management workstation.</span></span>

  - <span data-ttu-id="04b6e-144">Uma implantação mista do Lync Server 2013 e do Skype for Business Server 2015 com as seguintes funções de servidor em pelo menos um site executando o Skype for Business Server 2015:</span><span class="sxs-lookup"><span data-stu-id="04b6e-144">A mixed Lync Server 2013 and Skype for Business Server 2015 deployment with the following server roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="04b6e-145">Pelo menos um servidor Pool Enterprise ou Standard Edition. </span><span class="sxs-lookup"><span data-stu-id="04b6e-145">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="04b6e-146">O Pool de Diretores associado à federação SIP, se ela existir.</span><span class="sxs-lookup"><span data-stu-id="04b6e-146">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="04b6e-147">O Pool de Borda associado à federação SIP.</span><span class="sxs-lookup"><span data-stu-id="04b6e-147">The Edge Pool associated with SIP federation</span></span>

  - <span data-ttu-id="04b6e-148">Uma implantação mista do Lync Server 2010 e do Skype for Business Server 2015 com as seguintes funções de servidores em pelo menos um site executando o Skype for Business Server 2015:</span><span class="sxs-lookup"><span data-stu-id="04b6e-148">A mixed Lync Server 2010 and Skype for Business Server 2015 deployment with the following servers roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="04b6e-149">Pelo menos um servidor Pool Enterprise ou Standard Edition. </span><span class="sxs-lookup"><span data-stu-id="04b6e-149">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="04b6e-150">O Pool de Diretores associado à federação SIP, se ela existir.</span><span class="sxs-lookup"><span data-stu-id="04b6e-150">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="04b6e-151">O Pool de Borda associado à federação SIP do site.</span><span class="sxs-lookup"><span data-stu-id="04b6e-151">The Edge Pool associated with SIP federation for the Site</span></span>

  - <span data-ttu-id="04b6e-152">Uma implantação mista do Lync Server 2010 e do Lync Server 2013 com as seguintes funções de servidor em pelo menos um site executando o Lync Server 2013:</span><span class="sxs-lookup"><span data-stu-id="04b6e-152">A mixed Lync Server 2010 and Lync Server 2013 deployment with the following server roles in at least one site running Lync Server 2013:</span></span>
    
      - <span data-ttu-id="04b6e-153">Pelo menos um servidor Pool Enterprise ou Standard Edition no site.</span><span class="sxs-lookup"><span data-stu-id="04b6e-153">At least one Enterprise Pool or Standard Edition server in the site</span></span>
    
      - <span data-ttu-id="04b6e-154">O Pool de Diretores associado à federação SIP, se ela existir no site.</span><span class="sxs-lookup"><span data-stu-id="04b6e-154">The Director Pool associated with SIP federation, if it exists in the site</span></span>
    
      - <span data-ttu-id="04b6e-155">O Pool de Borda associado à federação SIP do site.</span><span class="sxs-lookup"><span data-stu-id="04b6e-155">The Edge Pool associated with SIP federation for the site</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="04b6e-156">Todo o gerenciamento de usuários, incluindo movimentações de usuários entre o local e o UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, precisa ser feito usando a versão mais recente instalada das ferramentas administrativas.</span><span class="sxs-lookup"><span data-stu-id="04b6e-156">All user management, including user moves between on-premises and UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, needs to be done using the latest installed version of the administrative tools.</span></span> <span data-ttu-id="04b6e-157">As ferramentas administrativas devem ser instaladas em um servidor separado que tenha acesso de conexão à implantação local existente e à Internet.</span><span class="sxs-lookup"><span data-stu-id="04b6e-157">The administrative tools must be installed on a separate server that has connect access to the existing on-premises deployment and to the Internet.</span></span> <span data-ttu-id="04b6e-158">O cmdlet <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> para mover usuários de sua implantação local para UNRESOLVED_TOKEN_VAL(skype16_online) deve ser executado a partir das ferramentas administrativas conectadas à sua implantação local.</span><span class="sxs-lookup"><span data-stu-id="04b6e-158">The <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> cmdlet to move users from your on-premises deployment to UNRESOLVED_TOKEN_VAL(skype16_online) must be run from the administrative tools connected to your on-premises deployment.</span></span>



</div>

<span data-ttu-id="04b6e-159">Para obter mais informações sobre topologias com suporte, consulte Topologias com suporte no [Lync Server 2013](lync-server-2013-supported-topologies.md)e topologias de referência do [Lync Server 2013](https://go.microsoft.com/fwlink/p/?linkid=398709)para implantações híbridas corporativas.</span><span class="sxs-lookup"><span data-stu-id="04b6e-159">For more information about supported topologies, see [Supported topologies in Lync Server 2013](lync-server-2013-supported-topologies.md), and [Lync Server 2013 Reference Topologies for Enterprise Hybrid Deployments](https://go.microsoft.com/fwlink/p/?linkid=398709).</span></span>

<span data-ttu-id="04b6e-160">Para obter informações de solução de problemas sobre implantações híbridas e conectar o PowerShell ao Lync Online, consulte [Lync Online: Lync PowerShell e Solução de Problemas Híbridos.](https://go.microsoft.com/fwlink/p/?linkid=306718)</span><span class="sxs-lookup"><span data-stu-id="04b6e-160">For troubleshooting information about hybrid deployments and connecting PowerShell to Lync Online, see [Lync Online: Lync PowerShell and Hybrid Troubleshooting](https://go.microsoft.com/fwlink/p/?linkid=306718).</span></span>

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a><span data-ttu-id="04b6e-161">Requisitos para listas de federação permitidos/bloqueados</span><span class="sxs-lookup"><span data-stu-id="04b6e-161">Requirements for Federation Allowed/Blocked Lists</span></span>

<span data-ttu-id="04b6e-p108">A lista Domínios permitidos contém domínios com um FQDN (nome de domínio totalmente qualificado) de Borda parceiro configurado. Por vezes, eles são chamados de *servidores parceiros permitidos* ou *parceiros de federação diretos*. Você deve estar familiarizado com a diferença entre a federação aberta e a federação fechada, conhecidas respectivamente como *descoberta de parceiros* e *lista de domínios dos parceiros permitidos* nas implantações locais.</span><span class="sxs-lookup"><span data-stu-id="04b6e-p108">The Allowed domains list includes domains that have a partner Edge fully qualified domain name (FQDN) configured. These are sometimes referred to as *allowed partner servers* or *direct federation partners*. You should be familiar with the difference between Open Federation and Closed Federation, referred to as *partner discovery* and *allowed partner domain list*, respectively, in on-premises deployments.</span></span>

<span data-ttu-id="04b6e-165">Os seguintes requisitos devem ser atendidos para configurar com êxito uma implantação híbrida:</span><span class="sxs-lookup"><span data-stu-id="04b6e-165">The following requirements must be met to successfully configure a hybrid deployment:</span></span>

  - <span data-ttu-id="04b6e-166">A correspondência de domínio deve ser configurada da mesma forma para sua implantação local e sua organização do Microsoft 365 ou office 365.</span><span class="sxs-lookup"><span data-stu-id="04b6e-166">Domain matching must be configured the same for your on-premises deployment and your Microsoft 365 or Office 365 organization.</span></span> <span data-ttu-id="04b6e-167">Se a descoberta de parceiros estiver habilitada na implantação local, a federação aberta deverá ser configurada para seu locatário online.</span><span class="sxs-lookup"><span data-stu-id="04b6e-167">If partner discovery is enabled on the on-premises deployment, then open federation must be configured for your online tenant.</span></span> <span data-ttu-id="04b6e-168">Caso contrário, a federação fechada deverá ser configurada para seu locatário online.</span><span class="sxs-lookup"><span data-stu-id="04b6e-168">If partner discovery is not enabled, then closed federation must be configured for your online tenant.</span></span>

  - <span data-ttu-id="04b6e-169">A lista de domínios bloqueados da implantação local deve corresponder exatamente à do seu locatário online.</span><span class="sxs-lookup"><span data-stu-id="04b6e-169">The Blocked domains list in the on-premises deployment must exactly match the Blocked domains list for your online tenant.</span></span>

  - <span data-ttu-id="04b6e-170">A lista de domínios permitidos da implantação local deve corresponder exatamente à do seu locatário online.</span><span class="sxs-lookup"><span data-stu-id="04b6e-170">The Allowed domains list in the on-premises deployment must exactly match the Allowed domains list for your online tenant.</span></span>

  - <span data-ttu-id="04b6e-171">A federação deve estar habilitada para as comunicações externas para o locatário online, que é configurada usando o Painel de Controle do Lync Online.</span><span class="sxs-lookup"><span data-stu-id="04b6e-171">Federation must be enabled for the external communications for the online tenant, which is configured by using the Lync Online Control Panel.</span></span>

</div>

<div>

## <a name="dns-settings"></a><span data-ttu-id="04b6e-172">Configurações dns</span><span class="sxs-lookup"><span data-stu-id="04b6e-172">DNS Settings</span></span>

<span data-ttu-id="04b6e-173">Ao criar registros DNS para implantações híbridas, todos os registros DNS externos do Lync devem apontar para a infraestrutura local.</span><span class="sxs-lookup"><span data-stu-id="04b6e-173">When creating DNS records for hybrid deployments, all Lync external DNS records should point to the on-premises infrastructure.</span></span> <span data-ttu-id="04b6e-174">Para obter detalhes sobre registros DNS necessários, consulte Requisitos do Sistema de Nomes de Domínio [(DNS) para o Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="04b6e-174">For details on required DNS records, please refer to [Domain Name System (DNS) requirements for Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md).</span></span>

<span data-ttu-id="04b6e-175">Além disso será necessário garantir que a resolução DNS descrita na tabela a seguir funciona em sua implantação local:</span><span class="sxs-lookup"><span data-stu-id="04b6e-175">Additionally you need to ensure that the DNS resolution described in the following table works in your on-premises deployment:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04b6e-176">Registro DNS</span><span class="sxs-lookup"><span data-stu-id="04b6e-176">DNS record</span></span></p></td>
<td><p><span data-ttu-id="04b6e-177">Pode ser resolvido por</span><span class="sxs-lookup"><span data-stu-id="04b6e-177">Resolvable by</span></span></p></td>
<td><p><span data-ttu-id="04b6e-178">Requisitos de DNS</span><span class="sxs-lookup"><span data-stu-id="04b6e-178">DNS requirement</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04b6e-179">Registro SRV DNS para _sipfederationtls._tcp. &lt; sipdomain.com para todos os domínios SIP com suporte &gt; que resolvem ip(s) externos do Access Edge</span><span class="sxs-lookup"><span data-stu-id="04b6e-179">DNS SRV record for _sipfederationtls._tcp.&lt;sipdomain.com&gt; for all supported SIP domains resolving to Access Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="04b6e-180">Servidor(es) de borda</span><span class="sxs-lookup"><span data-stu-id="04b6e-180">Edge server(s)</span></span></p></td>
<td><p><span data-ttu-id="04b6e-p111">Habilitar a comunicação federada em uma configuração híbrida. O servidor de borda precisa saber para onde encaminhar o tráfego federado para o domínio SIP que está dividido entre as instalações local e online.</span><span class="sxs-lookup"><span data-stu-id="04b6e-p111">Enable federated communication in a hybrid configuration. The Edge Server needs to know where to route federated traffic for the SIP domain that is split between on premises and online.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04b6e-183">Registro(s) A de DNS para FQDN do serviço de webconferência de borda, como webcon.contoso.com, que resolve IP(s) de borda de webconferência</span><span class="sxs-lookup"><span data-stu-id="04b6e-183">DNS A record(s) for Edge Web Conferencing Service FQDN, e.g. webcon.contoso.com resolving to Web Conferencing Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="04b6e-184">Computadores de usuários conectados à rede corporativa interna</span><span class="sxs-lookup"><span data-stu-id="04b6e-184">Internal corporate network connected users’ computers</span></span></p></td>
<td><p><span data-ttu-id="04b6e-p112">Habilitar usuários online para apresentar ou visualizar conteúdo em reuniões hospedadas localmente. O conteúdo inclui arquivos do PowerPoint, quadros de comunicações, votações e observações compartilhadas. </span><span class="sxs-lookup"><span data-stu-id="04b6e-p112">Enable online users to present or view content in on-premises hosted meetings. Content includes PowerPoint files, whiteboards, polls, and shared notes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="04b6e-187">Dependendo de como o DNS está configurado na sua organização, talvez seja necessário adicionar esses registros à zona DNS hospedada interna para os domínios SIP correspondentes para proporcionar resolução de DNS interna para esses registros.</span><span class="sxs-lookup"><span data-stu-id="04b6e-187">Depending on how DNS is configured in your organization, you may need to add these records to the internal hosted DNS zone for the corresponding SIP domain(s) to provide internal DNS resolution to these records.</span></span>

</div>

<div>

## <a name="firewall-considerations"></a><span data-ttu-id="04b6e-188">Considerações sobre firewall</span><span class="sxs-lookup"><span data-stu-id="04b6e-188">Firewall Considerations</span></span>

<span data-ttu-id="04b6e-p113">Os computadores de sua rede devem ser capazes de realizar pesquisas DNS padrão na Internet. Se esses computadores puderem acessar os sites padrão da Internet, sua rede atenderá a esse requisito.</span><span class="sxs-lookup"><span data-stu-id="04b6e-p113">Computers on your network must be able to perform standard Internet DNS lookups. If these computers can reach standard Internet sites, your network meets this requirement.</span></span>

<span data-ttu-id="04b6e-191">Dependendo do local do seu data center Microsoft Online Services, você também deve configurar seus dispositivos de firewall de rede para aceitar conexões com base em nomes de domínio curinga (por exemplo, todo o tráfego de \* .outlook.com).</span><span class="sxs-lookup"><span data-stu-id="04b6e-191">Depending on the location of your Microsoft Online Services data center, you must also configure your network firewall devices to accept connections based on wildcard domain names (for example, all traffic from \*.outlook.com).</span></span> <span data-ttu-id="04b6e-192">Se os firewalls de sua organização não oferecem suporte às configurações de nome com coringa, você deve determinar manualmente o intervalo de endereço IP que deseja permitir e as portas especificadas.</span><span class="sxs-lookup"><span data-stu-id="04b6e-192">If your organization’s firewalls do not support wildcard name configurations, you will have to manually determine the IP address ranges that you would like to allow and the specified ports.</span></span>

<span data-ttu-id="04b6e-193">Consulte o tópico Ajuda URLs e intervalos de [endereços IP do Office 365.](https://go.microsoft.com/fwlink/p/?linkid=252942)</span><span class="sxs-lookup"><span data-stu-id="04b6e-193">Refer to the Help topic [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=252942).</span></span>

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a><span data-ttu-id="04b6e-194">Requisitos de porta e protocolo</span><span class="sxs-lookup"><span data-stu-id="04b6e-194">Port and Protocol Requirements</span></span>

<span data-ttu-id="04b6e-195">Além dos requisitos de porta para comunicação interna do Lync Server 2013, você também deve configurar as portas a seguir.</span><span class="sxs-lookup"><span data-stu-id="04b6e-195">In addition to the port requirements for internal Lync Server 2013 communication, you must also configure the following ports.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04b6e-196">Protocolo/Porta</span><span class="sxs-lookup"><span data-stu-id="04b6e-196">Protocol / Port</span></span></th>
<th><span data-ttu-id="04b6e-197">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="04b6e-197">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04b6e-198">TCP 443</span><span class="sxs-lookup"><span data-stu-id="04b6e-198">TCP 443</span></span></p></td>
<td><p><span data-ttu-id="04b6e-199">Abrir entrada</span><span class="sxs-lookup"><span data-stu-id="04b6e-199">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="04b6e-200">Serviços de Federação do Active Directory (função de servidor de federação)</span><span class="sxs-lookup"><span data-stu-id="04b6e-200">Active Directory Federation Services (federation server role)</span></span></p>
<p><span data-ttu-id="04b6e-201">Para obter mais informações, consulte <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Understanding AD FS Role Services</a>.</span><span class="sxs-lookup"><span data-stu-id="04b6e-201">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Understanding AD FS Role Services</a>.</span></span></p></li>
<li><p><span data-ttu-id="04b6e-202">Serviços de Federação do Active Directory (função de servidor proxy)</span><span class="sxs-lookup"><span data-stu-id="04b6e-202">Active Directory Federation Services (proxy server role)</span></span></p></li>
<li><p><span data-ttu-id="04b6e-203">Microsoft Online Services Portal</span><span class="sxs-lookup"><span data-stu-id="04b6e-203">Microsoft Online Services Portal</span></span></p></li>
<li><p><span data-ttu-id="04b6e-204">Portal da Minha Empresa</span><span class="sxs-lookup"><span data-stu-id="04b6e-204">My Company Portal</span></span></p></li>
<li><p><span data-ttu-id="04b6e-205">Outlook Web App</span><span class="sxs-lookup"><span data-stu-id="04b6e-205">Outlook Web App</span></span></p></li>
<li><p><span data-ttu-id="04b6e-206">Cliente Lync (comunicação com o Lync Online a partir do Lync Server local)</span><span class="sxs-lookup"><span data-stu-id="04b6e-206">Lync client (communication to Lync Online from on-premises Lync Server)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04b6e-207">TCP 80 e 443</span><span class="sxs-lookup"><span data-stu-id="04b6e-207">TCP 80 and 443</span></span></p></td>
<td><p><span data-ttu-id="04b6e-208">Abrir entrada</span><span class="sxs-lookup"><span data-stu-id="04b6e-208">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="04b6e-209">Ferramenta de Sincronização de Diretórios do Microsoft Online Services</span><span class="sxs-lookup"><span data-stu-id="04b6e-209">Microsoft Online Services Directory Synchronization Tool</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04b6e-210">TCP 5061</span><span class="sxs-lookup"><span data-stu-id="04b6e-210">TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="04b6e-211">Abrir entrada/saída no Servidor de Borda</span><span class="sxs-lookup"><span data-stu-id="04b6e-211">Open inbound/outbound on the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04b6e-212">PSOM/TLS 443</span><span class="sxs-lookup"><span data-stu-id="04b6e-212">PSOM/TLS 443</span></span></p></td>
<td><p><span data-ttu-id="04b6e-213">Abrir entrada/saída para sessões de compartilhamento de dados</span><span class="sxs-lookup"><span data-stu-id="04b6e-213">Open inbound/outbound for data sharing sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04b6e-214">STUN/TCP 443</span><span class="sxs-lookup"><span data-stu-id="04b6e-214">STUN/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="04b6e-215">Abrir sessões de entrada/saída para áudio, vídeo, compartilhamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="04b6e-215">Open inbound/outbound for audio, video, application sharing sessions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04b6e-216">STUN/UDP 3478</span><span class="sxs-lookup"><span data-stu-id="04b6e-216">STUN/UDP 3478</span></span></p></td>
<td><p><span data-ttu-id="04b6e-217">Abrir entrada/saída para sessões de áudio e vídeo</span><span class="sxs-lookup"><span data-stu-id="04b6e-217">Open inbound/outbound for audio and video sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04b6e-218">RTP/TCP 50000-59999</span><span class="sxs-lookup"><span data-stu-id="04b6e-218">RTP/TCP 50000-59999</span></span></p></td>
<td><p><span data-ttu-id="04b6e-219">Abrir saída para sessões de áudio e vídeo</span><span class="sxs-lookup"><span data-stu-id="04b6e-219">Open outbound for audio and video sessions</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a><span data-ttu-id="04b6e-220">Contas de usuário e dados</span><span class="sxs-lookup"><span data-stu-id="04b6e-220">User Accounts and Data</span></span>

<span data-ttu-id="04b6e-221">Em uma implantação híbrida do Lync Server 2013, qualquer usuário que você deseja ter no Lync Online deve primeiro ser criado na implantação local, para que a conta de usuário seja criada nos Serviços de Domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="04b6e-221">In a Lync Server 2013 hybrid deployment, any user that you want to home in Lync Online must first be created in the on-premises deployment, so that the user account is created in Active Directory Domain Services.</span></span> <span data-ttu-id="04b6e-222">Em seguida, você pode mover o usuário para o Skype for Business Online, que move a lista de contatos do usuário.</span><span class="sxs-lookup"><span data-stu-id="04b6e-222">You can then move the user to Skype for Business Online, which will move the user’s contact list.</span></span>

<span data-ttu-id="04b6e-223">Ao sincronizar as contas de usuário entre suas implantações do Lync local e do Lync Online com o AD FS e o Dirsync, você precisa sincronizar as contas do AD para todos os usuários do Lync em sua organização entre suas implantações locais e online do Lync, mesmo que os usuários não sejam movidos para o Lync Online.</span><span class="sxs-lookup"><span data-stu-id="04b6e-223">When you synchronize user accounts between your Lync on-premises and Lync Online deployments with AD FS and Dirsync, you need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="04b6e-224">Se você não sincronizar todos os usuários, a comunicação entre os usuários locais e online na sua organização poderá não funcionar conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="04b6e-224">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="04b6e-225">Se o usuário for criado usando o portal online para o Centro de administração do Microsoft 365, a conta de usuário não será sincronizada com o Active Directory local e o usuário não existirá no Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="04b6e-225">If the user is created by using the online portal for Microsoft 365 admin center, the user account will not be synchronized with on-premises Active Directory, and the user will not exist in the on-premises Active Directory.</span></span> <span data-ttu-id="04b6e-226">Se você já criou usuários no Lync Online e deseja configurar híbrido com um Lync Server local, consulte Mover usuários do Lync Online para o Lync local no <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="04b6e-226">If you have already created users in Lync Online, and want to configure hybrid with an on-premises Lync Server, see <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Moving users from Lync Online to Lync on-premises in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="04b6e-227">Você também deve considerar os seguintes problemas relacionados ao usuário ao se planejar para uma implantação híbrida.</span><span class="sxs-lookup"><span data-stu-id="04b6e-227">You should also consider the following user-related issues when planning for a hybrid deployment.</span></span>

  - <span data-ttu-id="04b6e-228">**Contatos do usuário**   O limite para contatos para usuários do Lync Online é 250.</span><span class="sxs-lookup"><span data-stu-id="04b6e-228">**User contacts**   The limit for contacts for Lync Online users is 250.</span></span> <span data-ttu-id="04b6e-229">Todos os contatos além desse número serão removidos da lista de contatos do usuário quando a conta for movida para o Lync Online.</span><span class="sxs-lookup"><span data-stu-id="04b6e-229">Any contacts beyond that number will be removed from the user’s contact list when the account is moved to Lync Online.</span></span>

  - <span data-ttu-id="04b6e-230">**Sistema de mensagens instantâneas e presença** As listas de contatos, os grupos e as ACLs (lista de controle de acesso) do usuário são migrados com a conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="04b6e-230">**Instant Messaging and Presence**   User contact lists, groups, and access control lists (ACLs) are migrated with the user account.</span></span>

  - <span data-ttu-id="04b6e-231">**Dados de conferência, conteúdo de reunião e reuniões agendadas**   Esse conteúdo não é migrado com a conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="04b6e-231">**Conferencing data, meeting content, and scheduled meetings**   This content is not migrated with the user account.</span></span> <span data-ttu-id="04b6e-232">Os usuários devem reagendar as reuniões depois que as contas são migradas para o Lync Online.</span><span class="sxs-lookup"><span data-stu-id="04b6e-232">Users must reschedule meetings after their accounts are migrated to Lync Online.</span></span>

</div>

<div>

## <a name="user-policies-and-features"></a><span data-ttu-id="04b6e-233">Políticas e recursos do usuário</span><span class="sxs-lookup"><span data-stu-id="04b6e-233">User Policies and Features</span></span>

  - <span data-ttu-id="04b6e-234">Em um ambiente híbrido do Lync Server 2013, os usuários podem ser habilitados para Mensagens Instantâneas, voz e reuniões no local ou online, mas não simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="04b6e-234">In a Lync Server 2013 hybrid environment, users can be enabled for Instant Messaging, voice, and meetings either on-premises or online, but not both simultaneously.</span></span>

  - <span data-ttu-id="04b6e-235">**Cliente Lync**    Alguns usuários podem exigir uma nova versão do cliente quando são movidos para o Lync Online.</span><span class="sxs-lookup"><span data-stu-id="04b6e-235">**Lync Client**    Some users may require a new client version when they are moved to Lync Online.</span></span> <span data-ttu-id="04b6e-236">Para o Office Communications Server 2007 R2, os usuários devem ser movidos para um pool do Lync Server 2013 antes da migração para o Lync Online.</span><span class="sxs-lookup"><span data-stu-id="04b6e-236">For Office Communications Server 2007 R2, users must be moved to a Lync Server 2013 pool prior to migration to Lync Online.</span></span>
    
    <span data-ttu-id="04b6e-237">Para obter mais informações sobre o suporte ao cliente, consulte [Clients for Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) and [Supported Lync clients and network port configurations](https://go.microsoft.com/fwlink/p/?linkid=281901).</span><span class="sxs-lookup"><span data-stu-id="04b6e-237">For more information about client support, see [Clients for Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) and [Supported Lync clients and network port configurations](https://go.microsoft.com/fwlink/p/?linkid=281901).</span></span>

  - <span data-ttu-id="04b6e-238">**Configuração e políticas locais (não usuário)**   As políticas online e local exigem configuração separada.</span><span class="sxs-lookup"><span data-stu-id="04b6e-238">**On-premises policies and configuration (non-user)**   Online and on-premises policies require separate configuration.</span></span> <span data-ttu-id="04b6e-239">Você não pode definir políticas globais que se apliquem a ambas.</span><span class="sxs-lookup"><span data-stu-id="04b6e-239">You cannot set global policies that apply to both.</span></span>

<span data-ttu-id="04b6e-240"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="04b6e-240"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
