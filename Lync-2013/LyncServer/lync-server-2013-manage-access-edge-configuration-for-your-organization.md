---
title: 'Lync Server 2013: Gerenciar configuração da borda de acesso para sua organização'
description: 'Lync Server 2013: gerenciar a configuração de borda de acesso para sua organização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage Access Edge Configuration for your organization
ms:assetid: 0145eb08-984f-4ecd-bf9c-364817619c2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552443(v=OCS.15)
ms:contentKeyID: 48679555
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2161385f9c03f025bcf6f5e599b7e0276f6d592c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426134"
---
# <a name="manage-access-edge-configuration-for-your-organization-in-lync-server-2013"></a><span data-ttu-id="0d171-103">Gerenciar configuração da borda de acesso para sua organização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0d171-103">Manage Access Edge Configuration for your organization in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0d171-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0d171-104">

<span> </span></span></span>

<span data-ttu-id="0d171-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="0d171-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="0d171-106">Esta documentação é preliminar e está sujeita a alterações.</span><span class="sxs-lookup"><span data-stu-id="0d171-106">This is preliminary documentation and is subject to change.</span></span> <span data-ttu-id="0d171-107">Os tópicos em branco são incluídos como espaços reservados.</span><span class="sxs-lookup"><span data-stu-id="0d171-107">Blank topics are included as placeholders.</span></span>

<span data-ttu-id="0d171-108">Após implantar um ou mais servidores Edge, você deve habilitar os tipos de acesso de domínio externo ou de provedor, acesso de usuário remoto e acesso de usuário anônimo a conferências por meio dos servidores de borda que terão suporte para sua organização.</span><span class="sxs-lookup"><span data-stu-id="0d171-108">After deploying one or more Edge Servers, you must enable the types of external domain or provider access, remote user access, and anonymous user access to conferences through the Edge Servers that will be supported for your organization.</span></span>

<span data-ttu-id="0d171-109">Essas opções incluem os seguintes tipos de acesso que podem ser configurados por meio da página de **configuração de borda de acesso** :</span><span class="sxs-lookup"><span data-stu-id="0d171-109">These options include the following types of access that can be configured through the **Access Edge Configuration** page:</span></span>

  - <span data-ttu-id="0d171-110">**Habilitar a conectividade de mensagens de chat pública e de Federação**   Habilite isso se você quiser dar suporte ao acesso de usuários a domínios de parceiros federados.</span><span class="sxs-lookup"><span data-stu-id="0d171-110">**Enable federation and public IM connectivity**   Enable this if you want to support user access to federated partner domains.</span></span> <span data-ttu-id="0d171-111">Essa configuração se aplica a agrupamentos SIP e a Federação XMPP configuradas para escopos global, de site ou de usuário na página **política de acesso externo** .</span><span class="sxs-lookup"><span data-stu-id="0d171-111">This setting applies to both SIP federation and XMPP federation that are configured for global, site or user scopes on the **External Access Policy** page.</span></span> <span data-ttu-id="0d171-112">Para que as configurações de Federação sejam aplicadas, você deve configurar o suporte de Federação em ambas as páginas.</span><span class="sxs-lookup"><span data-stu-id="0d171-112">For federation settings to apply, you must configure federation support on both pages.</span></span>
    
    <span data-ttu-id="0d171-113">Há duas opções que são configurações opcionais para o modo como os parceiros federados são descobertos e se o arquivamento de avisos de isenção de responsabilidade (notificação para contatos federados que você se comunica com essa implantação tem o arquivamento habilitado e se os detalhes de comunicação serão arquivados) serão enviados aos contatos</span><span class="sxs-lookup"><span data-stu-id="0d171-113">Two options exist that are optional settings for how federated partners are discovered, and whether archiving disclaimers (notification to federated contacts that you communicate with that your deployment has archiving enabled and that the communications details will be archived) will be sent to contacts</span></span>
    
      - <span data-ttu-id="0d171-114">**Habilitar a descoberta de domínio de parceiro**   Selecionar essa opção permite a descoberta automática de domínios com os quais você pode federar.</span><span class="sxs-lookup"><span data-stu-id="0d171-114">**Enable partner domain discovery**   Selecting this option enables the automatic discovery of domains that you can federate with.</span></span> <span data-ttu-id="0d171-115">O Lync Server 2013 usa registros de sistema de nomes de domínio (DNS) para tentar descobrir domínios que não estão listados na lista de domínios permitidos, avaliando automaticamente o tráfego de entrada de parceiros federados descobertos e limitando ou bloqueando esse tráfego com base no nível de confiança, na quantidade de tráfego e nas configurações do administrador.</span><span class="sxs-lookup"><span data-stu-id="0d171-115">Lync Server 2013 uses Domain Name System (DNS) records to try to discover domains not listed in the allowed domains list, automatically evaluating incoming traffic from discovered federated partners and limiting or blocking that traffic based on trust level, amount of traffic, and administrator settings.</span></span> <span data-ttu-id="0d171-116">Se você não selecionar essa opção, o acesso do usuário federado será habilitado somente para os usuários nos domínios que você incluir na lista de domínios permitidos.</span><span class="sxs-lookup"><span data-stu-id="0d171-116">If you do not select this option, federated user access is enabled only for users in the domains that you include on the allowed domains list.</span></span> <span data-ttu-id="0d171-117">Independentemente de você selecionar essa opção, você pode especificar que domínios individuais sejam bloqueados ou permitidos, incluindo a restrição de acesso a servidores específicos que executam o serviço de borda de acesso no domínio federado.</span><span class="sxs-lookup"><span data-stu-id="0d171-117">Whether or not you select this option, you can specify that individual domains to be blocked or allowed, including restricting access to specific servers running the Access Edge service in the federated domain.</span></span> <span data-ttu-id="0d171-118">Para obter detalhes, consulte [Configurar o suporte para domínios externos permitidos no Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md).</span><span class="sxs-lookup"><span data-stu-id="0d171-118">For details, see [Configure support for allowed external domains in Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md).</span></span>
    
      - <span data-ttu-id="0d171-119">**Enviar isenção de responsabilidade de arquivamento para parceiros federados**   Selecionar essa opção permite o envio de uma mensagem de isenção de isenção de responsabilidade para parceiros federados que os aconselha a gravar os dados de comunicação.</span><span class="sxs-lookup"><span data-stu-id="0d171-119">**Send archiving disclaimer to federated partners**   Selecting this option enables the sending of an archiving disclaimer message to federated partners that advises them that communications details are recorded.</span></span> <span data-ttu-id="0d171-120">Se você arquivar comunicações externas com domínios de parceiros federados, habilite a notificação de isenção de isenção de responsabilidade para avisar os parceiros de que suas mensagens e os detalhes de comunicação estão sendo arquivados pela sua implantação.</span><span class="sxs-lookup"><span data-stu-id="0d171-120">If you archive external communications with federated partner domains, you should enable the archiving disclaimer notification to warn partners that their messages and communications details are being archived by your deployment.</span></span> <span data-ttu-id="0d171-121">Para obter detalhes sobre o arquivamento, consulte [definindo seus requisitos para arquivamento no Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="0d171-121">For details on archiving, see [Defining your requirements for Archiving in Lync Server 2013](lync-server-2013-defining-your-requirements-for-archiving.md).</span></span>

  - <span data-ttu-id="0d171-122">**Habilitar o acesso de usuários remotos**   Habilite esta opção se quiser que os usuários da organização que estão fora do seu firewall, como telecomutadores e usuários que estiverem viajando, possam se conectar ao Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0d171-122">**Enable remote user access**   Enable this option if you want users in your organization who are outside your firewall, such as telecommuters and users who are traveling, to be able to connect to Lync Server.</span></span> <span data-ttu-id="0d171-123">Para obter detalhes, consulte [habilitar ou desabilitar o acesso de usuário remoto no Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="0d171-123">For details, see [Enable or disable remote user access in Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md).</span></span>

  - <span data-ttu-id="0d171-124">**Permitir que usuários anônimos acessem conferências**   Habilite esta opção se quiser que os usuários internos convidem usuários anônimos externos para conferências que eles organizam.</span><span class="sxs-lookup"><span data-stu-id="0d171-124">**Enable anonymous users to access conferences**   Enable this option if you want internal users to invite external anonymous users to conferences that they organize.</span></span> <span data-ttu-id="0d171-125">Habilitar essa configuração só permite usuários anônimos para conferências.</span><span class="sxs-lookup"><span data-stu-id="0d171-125">Enabling this setting only allows anonymous users for conferences.</span></span> <span data-ttu-id="0d171-126">Para configurar a experiência de conferência e as opções que definirão como e o que os usuários podem fazer com conferências e para a inclusão de usuários anônimos, consulte detalhes em [criar ou modificar a experiência do usuário de conferência para uma](https://technet.microsoft.com/library/gg429715\(v=ocs.15\)) referência de política de site ou usuários e [conferência para o Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span><span class="sxs-lookup"><span data-stu-id="0d171-126">To configure the conferencing experience and options that will define how and what your users can do with conferences and for the inclusion of anonymous users, see details at [Create or Modify Conferencing User Experience for a Site or Users](https://technet.microsoft.com/library/gg429715\(v=ocs.15\)) and [Conferencing policy settings reference for Lync Server 2013](lync-server-2013-conferencing-policy-settings-reference.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0d171-127">Além de habilitar o suporte a acesso externo do usuário, você também pode configurar políticas para controlar o uso do acesso de usuários remotos em sua organização antes de qualquer tipo de acesso de usuário externo estar disponível para os usuários.</span><span class="sxs-lookup"><span data-stu-id="0d171-127">In addition to enabling external user access support, you also configure policies to control the use of remote user access in your organization before any type of external user access is available to users.</span></span> <span data-ttu-id="0d171-128">Para obter detalhes sobre como criar, configurar e aplicar políticas para acesso externo a usuários, consulte <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">gerenciar a política de acesso externo no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="0d171-128">For details about creating, configuring, and applying policies for external user access, see <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">Manage external access policy in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="0d171-129">**Exibindo informações de configuração de borda de acesso usando cmdlets do Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="0d171-129">**Viewing Access Edge configuration information by using Windows PowerShell cmdlets**</span></span>

  - <span data-ttu-id="0d171-130">As informações de configuração de borda de acesso podem ser exibidas usando o Windows PowerShell e o cmdlet **Get-CsAccessEdgeConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="0d171-130">Access Edge configuration information can be viewed by using Windows PowerShell and the **Get-CsAccessEdgeConfiguration** cmdlet.</span></span> <span data-ttu-id="0d171-131">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d171-131">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="0d171-132">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="0d171-132">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>
    
    <span data-ttu-id="0d171-133">Para ver informações sobre todas as suas configurações de borda de acesso, digite o seguinte comando no Shell de gerenciamento do Lync Server e pressione ENTER:</span><span class="sxs-lookup"><span data-stu-id="0d171-133">To view information about all your Access Edge configuration settings, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsAccessEdgeConfiguration
    
    <span data-ttu-id="0d171-134">Isso retornará informações parecidas com:</span><span class="sxs-lookup"><span data-stu-id="0d171-134">That will return information similar to this:</span></span>
    
        Identity                               : Global
        AllowAnonymousUsers                    : False
        AllowFederatedUsers                    : False
        AllowOutsideUsers                      : True
        BeClearingHouse                        : False
        EnablePartnerDiscovery                 : False
        EnableArchivingDisclaimer              : False
        EnableUserReplicator                   : True
        KeepCrlsUpToDateForPeers               : True
        MarkSourceVerifiableOnOutgoingMessages : True
        OutgoingTlsCountForFederatedPartners   : 4
        DiscoveredPartnerStandardRate          : 20
        EnableDiscoveredPartnerContactsLimit   : True
        MaxContactsPerDiscoveredPartner        : 1000
        DiscoveredPartnerReportPeriodMinutes   : 60
        MaxAcceptedCertificatesStored          : 1000
        MaxRejectedCertificatesStored          : 500
        CertificatesDeletedPercentage          : 20
        RoutingMethod                          : UseDnsSrvRouting

<div>

## <a name="in-this-section"></a><span data-ttu-id="0d171-135">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0d171-135">In This Section</span></span>

  - [<span data-ttu-id="0d171-136">Habilitar ou desabilitar federação e conectividade de IM pública no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0d171-136">Enable or disable federation and public IM connectivity in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)

  - [<span data-ttu-id="0d171-137">Habilitar ou desabilitar descoberta de parceiros de federação no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0d171-137">Enable or disable discovery of federation partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md)

  - [<span data-ttu-id="0d171-138">Habilitar ou desabilitar o envio de um aviso de isenção de responsabilidade de Arquivamento a parceiros federados no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0d171-138">Enable or disable sending an Archiving disclaimer to federated partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-sending-an-archiving-disclaimer-to-federated-partners.md)

  - [<span data-ttu-id="0d171-139">Habilitar ou desabilitar acesso de usuário remoto no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0d171-139">Enable or disable remote user access in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-remote-user-access.md)

  - [<span data-ttu-id="0d171-140">Habilitar ou desabilitar acesso de usuário anônimo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0d171-140">Enable or disable anonymous user access in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-anonymous-user-access.md)

  - [<span data-ttu-id="0d171-141">Atribuir políticas de conferência para suporte de usuários anônimos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0d171-141">Assign conferencing policies to support anonymous users in Lync Server 2013</span></span>](lync-server-2013-assign-conferencing-policies-to-support-anonymous-users.md)

<span data-ttu-id="0d171-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0d171-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

