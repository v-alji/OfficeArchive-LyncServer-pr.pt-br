---
title: 'Lync Server 2013: Habilitar ou desabilitar federação e conectividade de IM pública'
description: 'Lync Server 2013: habilitar ou desabilitar a conectividade de mensagens de chat públicas e a Federação.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable federation and public IM connectivity
ms:assetid: 8ec58f4b-9f6d-47b4-a187-d18a83fe4577
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182549(v=OCS.15)
ms:contentKeyID: 48184813
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 48c77e4bf892fa891f413226a4adf068e980c352
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437543"
---
# <a name="enable-or-disable-federation-and-public-im-connectivity-in-lync-server-2013"></a><span data-ttu-id="2d091-103">Habilitar ou desabilitar federação e conectividade de IM pública no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2d091-103">Enable or disable federation and public IM connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2d091-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2d091-104">

<span> </span></span></span>

<span data-ttu-id="2d091-105">_**Tópico da última modificação:** 2013-06-24_</span><span class="sxs-lookup"><span data-stu-id="2d091-105">_**Topic Last Modified:** 2013-06-24_</span></span>

<span data-ttu-id="2d091-106">O suporte para Federação é necessário para habilitar os usuários que têm uma conta com um cliente ou uma organização de parceiros confiáveis, incluindo domínios de parceiros e usuários de provedores de serviços de mensagens instantâneas (IM) que você dá suporte a colaborar com os usuários da sua organização.</span><span class="sxs-lookup"><span data-stu-id="2d091-106">Support for federation is required to enable users who have an account with a trusted customer or partner organization, including partner domains and users of public instant messaging (IM) provider users that you support, to collaborate with users in your organization.</span></span> <span data-ttu-id="2d091-107">A Federação também é necessária para usar um provedor de serviços do Exchange hospedado para fornecer correio de voz para usuários do Enterprise Voice cujas caixas de correio estão localizadas em um serviço hospedado do Exchange, como o Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2d091-107">Federation is also required to use a hosted Exchange service provider to provide voice mail to Enterprise Voice users whose mailboxes are located on a hosted Exchange service such as Microsoft Exchange Online.</span></span> <span data-ttu-id="2d091-108">Quando tiver estabelecido uma relação de confiança com esses domínios externos, você poderá autorizar os usuários desses domínios a acessarem sua implantação e participar de comunicações do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2d091-108">When you have established a trust relationship with these external domains, you can authorize users in those domains to access your deployment and participate in Lync Server communications.</span></span> <span data-ttu-id="2d091-109">Essa relação de confiança é chamada de Federação e não é relacionada à relação de confiança do Active Directory, ou depende dela.</span><span class="sxs-lookup"><span data-stu-id="2d091-109">This trust relationship is called a federation and it is not related to, or dependent upon, an Active Directory trust relationship.</span></span>

<span data-ttu-id="2d091-110">Para dar suporte ao acesso por usuários de domínios federados, você deve habilitar a Federação.</span><span class="sxs-lookup"><span data-stu-id="2d091-110">To support access by users of federated domains, you must enable federation.</span></span> <span data-ttu-id="2d091-111">Se você habilitar a Federação para sua organização, também deverá especificar se deseja implementar as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="2d091-111">If you enable federation for your organization, you must also specify whether to implement the following options:</span></span>

  - <span data-ttu-id="2d091-112">**Habilitar a descoberta de domínio de parceiro**   Se você habilitar essa opção, o Lync Server usará os registros de sistema de nome de domínio (DNS) para tentar descobrir domínios não listados na lista de domínios permitidos, avaliando automaticamente o tráfego de entrada de parceiros federados descobertos e limitando ou bloqueando esse tráfego com base no nível de confiança, na quantidade de tráfego e nas configurações do administrador.</span><span class="sxs-lookup"><span data-stu-id="2d091-112">**Enable partner domain discovery**   If you enable this option, Lync Server uses Domain Name System (DNS) records to try to discover domains not listed in the allowed domains list, automatically evaluating incoming traffic from discovered federated partners and limiting or blocking that traffic based on trust level, amount of traffic, and administrator settings.</span></span> <span data-ttu-id="2d091-113">Se você não selecionar essa opção, o acesso do usuário federado será habilitado somente para os usuários nos domínios que você incluir na lista de domínios permitidos.</span><span class="sxs-lookup"><span data-stu-id="2d091-113">If you do not select this option, federated user access is enabled only for users in the domains that you include on the allowed domains list.</span></span> <span data-ttu-id="2d091-114">Independentemente de você selecionar essa opção, você pode especificar que domínios individuais sejam bloqueados ou permitidos, incluindo a restrição de acesso a servidores específicos que executam o serviço de borda de acesso no domínio federado.</span><span class="sxs-lookup"><span data-stu-id="2d091-114">Whether or not you select this option, you can specify that individual domains to be blocked or allowed, including restricting access to specific servers running the Access Edge service in the federated domain.</span></span> <span data-ttu-id="2d091-115">Para obter detalhes sobre o controle do acesso a domínios federados, consulte [Configurar o suporte para domínios externos permitidos no Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md).</span><span class="sxs-lookup"><span data-stu-id="2d091-115">For details about controlling access by federated domains, see [Configure support for allowed external domains in Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md).</span></span>

  - <span data-ttu-id="2d091-116">**Enviar uma isenção de responsabilidade de arquivamento para parceiros federados**    Aviso de isenção de responsabilidade é enviado para parceiros federados que o arquivamento em sua implantação está em vigor.</span><span class="sxs-lookup"><span data-stu-id="2d091-116">**Send an archiving disclaimer to federated partners**    Disclaimer notice is sent to federated partners that archiving in your deployment is in place.</span></span> <span data-ttu-id="2d091-117">Se você oferecer suporte ao arquivamento de comunicações externas com domínios de parceiros federados, habilite a notificação de exclusão de isenção de arquivo para avisar os parceiros de que suas mensagens estão sendo arquivadas.</span><span class="sxs-lookup"><span data-stu-id="2d091-117">If you support archiving of external communications with federated partner domains, you should enable the archiving disclaimer notification to warn partners that their messages are being archived.</span></span>

<span data-ttu-id="2d091-118">Se, mais tarde, você quiser impedir o acesso temporário ou permanente por usuários de domínios federados, poderá desabilitar a Federação para a sua organização.</span><span class="sxs-lookup"><span data-stu-id="2d091-118">If you later want to temporarily or permanently prevent access by users of federated domains, you can disable federation for your organization.</span></span> <span data-ttu-id="2d091-119">Use o procedimento desta seção para habilitar ou desabilitar o acesso de usuário federado à sua organização, incluindo a especificação das opções de Federação adequadas para ter suporte para sua organização.</span><span class="sxs-lookup"><span data-stu-id="2d091-119">Use the procedure in this section to enable or disable federated user access for your organization, including specifying the appropriate federation options to be supported for your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2d091-120">Habilitar a Federação para a sua organização especifica apenas que os servidores que executam o serviço de borda de acesso dão suporte a roteamento para domínios federados.</span><span class="sxs-lookup"><span data-stu-id="2d091-120">Enabling federation for your organization only specifies that your servers running the Access Edge service support routing to federated domains.</span></span> <span data-ttu-id="2d091-121">Os usuários em domínios federados não podem participar de mensagens instantâneas nem conferências em sua organização até você também configurar pelo menos uma política para dar suporte ao acesso de usuários federados.</span><span class="sxs-lookup"><span data-stu-id="2d091-121">Users in federated domains cannot participate in IM or conferences in your organization until you also configure at least one policy to support federated user access.</span></span> <span data-ttu-id="2d091-122">Os usuários de provedores de serviços públicos de mensagens instantâneas não podem participar de mensagens instantâneas nem conferências em sua organização até você também configurar pelo menos uma política para dar suporte à conectividade de mensagens de chat públicas.</span><span class="sxs-lookup"><span data-stu-id="2d091-122">Users of public IM service providers cannot participate in IM or conferences in your organization until you also configure at least one policy to support public IM connectivity.</span></span> <span data-ttu-id="2d091-123">O Lync Server não pode usar um serviço hospedado do Exchange para fornecer atendimento de chamada, Outlook Voice Access (incluindo correio de voz) ou serviços de atendedor automático para usuários cujas caixas de correio estão localizadas em um serviço do Exchange hospedado até você configurar uma política de caixa postal hospedada que forneça informações de roteamento.</span><span class="sxs-lookup"><span data-stu-id="2d091-123">Lync Server cannot use a hosted Exchange service to provide call answering, Outlook Voice Access (including voice mail), or auto-attendant services for users whose mailboxes are located on a hosted Exchange service until you configure a hosted voice mail policy that provides routing information.</span></span> <span data-ttu-id="2d091-124">Para obter detalhes sobre como configurar políticas para comunicação com usuários de domínios federados em outras organizações, consulte <A href="lync-server-2013-manage-sip-federated-domains-for-your-organization.md">gerenciar domínios federados SIP para sua organização no Lync Server 2013</A> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="2d091-124">For details about configuring policies for communication with users of federated domains in other organizations, see <A href="lync-server-2013-manage-sip-federated-domains-for-your-organization.md">Manage SIP federated domains for your organization in Lync Server 2013</A> in the Operations documentation.</span></span> <span data-ttu-id="2d091-125">Além disso, se quiser dar suporte à comunicação com usuários de provedores de serviços de mensagens instantâneas, você deve configurar políticas para dar suporte a ele e também configurar o suporte para provedores de serviços individuais aos quais você deseja dar suporte.</span><span class="sxs-lookup"><span data-stu-id="2d091-125">Additionally, if you want to support communication with users of IM service providers, you must configure policies to support it and also configure support for the individual service providers that you want to support.</span></span> <span data-ttu-id="2d091-126">Para obter detalhes, consulte <A href="lync-server-2013-manage-sip-federated-providers-for-your-organization.md">gerenciar provedores federados SIP para sua organização no Lync Server 2013</A> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="2d091-126">For details, see <A href="lync-server-2013-manage-sip-federated-providers-for-your-organization.md">Manage SIP federated providers for your organization in Lync Server 2013</A> in the Operations documentation.</span></span> <span data-ttu-id="2d091-127">Para obter detalhes sobre como criar uma política de caixa postal hospedada, consulte <A href="lync-server-2013-manage-hosted-voice-mail-policies.md">gerenciar políticas de caixa postal hospedadas no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="2d091-127">For details about creating a hosted voice mail policy, see <A href="lync-server-2013-manage-hosted-voice-mail-policies.md">Manage hosted voice mail policies in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="to-enable-or-disable-federated-user-access-for-your-organization"></a><span data-ttu-id="2d091-128">Para habilitar ou desabilitar o acesso de usuário federado à sua organização</span><span class="sxs-lookup"><span data-stu-id="2d091-128">To enable or disable federated user access for your organization</span></span>

1.  <span data-ttu-id="2d091-129">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="2d091-129">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="2d091-130">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="2d091-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="2d091-131">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2d091-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="2d091-132">Na barra de navegação à esquerda, clique em **acesso de usuário externo** e, em seguida, clique em **configuração de borda de acesso**.</span><span class="sxs-lookup"><span data-stu-id="2d091-132">In the left navigation bar, click **External User Access**, and then click **Access Edge Configuration**.</span></span>

4.  <span data-ttu-id="2d091-133">Na página **configuração de borda de acesso** , clique em **global**, clique em **Editar** e, em seguida, clique em **Mostrar detalhes**.</span><span class="sxs-lookup"><span data-stu-id="2d091-133">On the **Access Edge Configuration** page, click **Global**, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="2d091-134">Em **Editar configuração de borda de acesso**, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="2d091-134">In **Edit Access Edge Configuration**, do one of the following:</span></span>
    
      - <span data-ttu-id="2d091-135">Para habilitar o acesso de usuário federado à sua organização, marque a caixa de seleção **habilitar comunicações com usuários federados** .</span><span class="sxs-lookup"><span data-stu-id="2d091-135">To enable federated user access for your organization, select the **Enable communications with federated users** check box.</span></span>
    
      - <span data-ttu-id="2d091-136">Para desabilitar o acesso de usuário federado à sua organização, desmarque a caixa de seleção **habilitar comunicações com usuários federados** .</span><span class="sxs-lookup"><span data-stu-id="2d091-136">To disable federated user access for your organization, clear the **Enable communications with federated users** check box.</span></span>

6.  <span data-ttu-id="2d091-137">Se você tiver marcado a caixa de seleção **habilitar comunicações com usuários federados** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2d091-137">If you selected the **Enable communications with federated users** check box, do the following:</span></span>
    
    1.  <span data-ttu-id="2d091-138">Se você quiser dar suporte à descoberta automática de domínios de parceiros, marque a caixa de seleção **habilitar descoberta de domínio de parceiro** .</span><span class="sxs-lookup"><span data-stu-id="2d091-138">If you want to support automatic discovery of partner domains, select the **Enable partner domain discovery** check box.</span></span>
    
    2.  <span data-ttu-id="2d091-139">Se a sua organização oferecer suporte para o arquivamento de comunicações externas, marque a caixa de seleção **Enviar isenção de arquivo para parceiros federados** .</span><span class="sxs-lookup"><span data-stu-id="2d091-139">If your organization supports archiving of external communications, select the **Send archiving disclaimer to federated partners** check box.</span></span>

7.  <span data-ttu-id="2d091-140">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="2d091-140">Click **Commit**.</span></span>

<span data-ttu-id="2d091-141">Para habilitar os usuários federados a colaborar com usuários em sua implantação do Lync Server 2013, você também deve configurar pelo menos uma política de acesso externo para dar suporte ao acesso de usuários federados.</span><span class="sxs-lookup"><span data-stu-id="2d091-141">To enable federated users to collaborate with users in your Lync Server 2013 deployment, you must also configure at least one external access policy to support federated user access.</span></span> <span data-ttu-id="2d091-142">Para obter detalhes, consulte [Configurar políticas para controlar o acesso de usuários federados no Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md) na documentação de implantação ou a documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="2d091-142">For details, see [Configure policies to control federated user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-federated-user-access.md) in the Deployment documentation or the Operations documentation.</span></span> <span data-ttu-id="2d091-143">Para controlar o acesso para domínios federados específicos, consulte [Configurar o suporte para domínios externos permitidos no Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md) na documentação de implantação ou documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="2d091-143">To control access for specific federated domains, see [Configure support for allowed external domains in Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md) in the Deployment documentation or Operations documentation.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-federation-and-public-im-connectivity-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="2d091-144">Habilitar ou desabilitar a conectividade de mensagens de chat pública e de Federação usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2d091-144">Enabling or Disabling Federation and Public IM Connectivity by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="2d091-145">A Federação e a conectividade de mensagens instantâneas públicas também podem ser gerenciadas usando o Windows PowerShell e o cmdlet Set-CsAccessEdgeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d091-145">Federation and public IM connectivity can also be managed by using Windows PowerShell and the Set-CsAccessEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="2d091-146">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2d091-146">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="2d091-147">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="2d091-147">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-federation-and-public-im-connectivity"></a><span data-ttu-id="2d091-148">Para habilitar a conectividade de mensagens de chat pública e de Federação</span><span class="sxs-lookup"><span data-stu-id="2d091-148">To enable federation and public IM connectivity</span></span>

  - <span data-ttu-id="2d091-149">Para habilitar a conectividade de mensagens de chat pública e de Federação, defina o valor da propriedade **AllowFederatedUsers** como True ($true):</span><span class="sxs-lookup"><span data-stu-id="2d091-149">To enable federation and public IM connectivity, set the value of the **AllowFederatedUsers** property to True ($True):</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True

</div>

<div>

## <a name="to-disable-federation-and-public-im-connectivity"></a><span data-ttu-id="2d091-150">Para desabilitar a conectividade de mensagens de chat pública e de Federação</span><span class="sxs-lookup"><span data-stu-id="2d091-150">To disable federation and public IM connectivity</span></span>

  - <span data-ttu-id="2d091-151">Para desabilitar a conectividade de mensagens de chat pública e de Federação, defina o valor da propriedade **AllowFederatedUsers** como False ($false):</span><span class="sxs-lookup"><span data-stu-id="2d091-151">To disable federation and public IM connectivity, set the value of the **AllowFederatedUsers** property to False ($False):</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $False

<span data-ttu-id="2d091-152"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2d091-152"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

