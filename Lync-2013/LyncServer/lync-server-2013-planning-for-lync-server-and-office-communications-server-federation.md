---
title: Planejando a Federação do Lync Server e do Office Communications Server
description: Planejando a Federação do Lync Server e do Office Communications Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Lync Server and Office Communications Server federation
ms:assetid: c9eaf06b-054f-41a4-ad0c-499400d6c4c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205335(v=OCS.15)
ms:contentKeyID: 48185640
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5d7385b8fde27446fb0648802544a8840a0f6276
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424538"
---
# <a name="planning-for-lync-server-2013-and-office-communications-server-federation"></a><span data-ttu-id="d0f14-103">Planejando a Federação do Lync Server 2013 e do Office Communications Server</span><span class="sxs-lookup"><span data-stu-id="d0f14-103">Planning for Lync Server 2013 and Office Communications Server federation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d0f14-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d0f14-104">

<span> </span></span></span>

<span data-ttu-id="d0f14-105">_**Tópico da última modificação:** 2013-02-13_</span><span class="sxs-lookup"><span data-stu-id="d0f14-105">_**Topic Last Modified:** 2013-02-13_</span></span>

<span data-ttu-id="d0f14-106">Federação entre o Microsoft Lync Server 2013, o Lync Server 2010 e o Office Communications Server oferece suporte a comunicações ponto a ponto e de vários participantes.</span><span class="sxs-lookup"><span data-stu-id="d0f14-106">Federation between Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server supports peer-to-peer and multi-party communications.</span></span> <span data-ttu-id="d0f14-107">As conversas ponto a ponto podem ser escalonadas para conversas com vários participantes, permitindo reuniões ad hoc.</span><span class="sxs-lookup"><span data-stu-id="d0f14-107">Peer-to-peer conversations can be escalated to multi-party conversations, allowing for ad hoc meetings.</span></span> <span data-ttu-id="d0f14-108">Reuniões: Webconferência ou conferências de áudio/visuais – podem ser programadas para incluir contatos dentro da sua organização e contatos em parceiros com os quais você se federa.</span><span class="sxs-lookup"><span data-stu-id="d0f14-108">Meetings – Web conferencing or audio/visual conferences – can be scheduled to include contacts inside your organization as well as contacts in partners that you federate with.</span></span>

<span data-ttu-id="d0f14-109">A Federação apareceu primeiro no Microsoft Office Live Communications Server 2005 e com suporte um tipo de Federação, Federação direta.</span><span class="sxs-lookup"><span data-stu-id="d0f14-109">Federation first appeared in Microsoft Office Live Communications Server 2005 and supported one kind of federation, Direct Federation.</span></span> <span data-ttu-id="d0f14-110">A Federação direta exigia que você saiba o domínio SIP (Session Initiation Protocol) do parceiro de Federação e o nome de domínio totalmente qualificado (FQDN) do servidor de borda do parceiro.</span><span class="sxs-lookup"><span data-stu-id="d0f14-110">Direct Federation required you to know the federation partner’s session initiation protocol (SIP) domain and the fully qualified domain name (FQDN) of the partner’s Edge Server.</span></span> <span data-ttu-id="d0f14-111">O Live Communications Server 2005 com SP1 introduziu tipos de Federação adicionais, todos os registros SRV do sistema de nome de domínio (DNS) necessários a serem publicados pelo parceiro federado para localizar o servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="d0f14-111">Live Communications Server 2005 with SP1 introduced additional federation types, all of which required domain name system (DNS) SRV records to be published by the federated partner to locate their Edge Server.</span></span> <span data-ttu-id="d0f14-112">A terminologia do lançamento era:</span><span class="sxs-lookup"><span data-stu-id="d0f14-112">The terminology for that release was:</span></span>

  - <span data-ttu-id="d0f14-113">*Abrir a Federação aprimorada*: aceitar qualquer nome de domínio SIP e usar o SRV DNS para localizar o servidor de borda de parceiro</span><span class="sxs-lookup"><span data-stu-id="d0f14-113">*Open Enhanced Federation*: Accept any SIP domain name and use DNS SRV to locate the partner Edge Server</span></span>

  - <span data-ttu-id="d0f14-114">*Federação aprimorada*: configurar o nome de domínio SIP do parceiro como um parceiro de Federação para a sua organização e usar o SRV DNS para localizar o servidor de borda de parceiro</span><span class="sxs-lookup"><span data-stu-id="d0f14-114">*Enhanced Federation*: Configure the partner’s SIP domain name as a federation partner for your organization and use DNS SRV to find the partner Edge Server</span></span>

  - <span data-ttu-id="d0f14-115">*Federação direta*: configurar o nome de domínio SIP do parceiro e o FQDN para o servidor de borda do parceiro</span><span class="sxs-lookup"><span data-stu-id="d0f14-115">*Direct Federation*: Configure the partner’s SIP domain name and the FQDN to the partner’s Edge Server</span></span>

  - <span data-ttu-id="d0f14-116">*Lista de permissões do servidor*: aceitar qualquer domínio, usar o SRV DNS para localizar o servidor de borda de um provedor de hospedagem ou um provedor de conectividade de mensagens instantâneas (IM) público</span><span class="sxs-lookup"><span data-stu-id="d0f14-116">*Server Allow List*: Accept any domain, use DNS SRV to find the Edge Server of a hosting provider or a public instant messaging (IM) connectivity provider</span></span>

<span data-ttu-id="d0f14-117">O Microsoft Office Communications Server 2007 introduziu o nome atualizado dos tipos de Federação para definir melhor o que cada tipo de Federação realmente realizou:</span><span class="sxs-lookup"><span data-stu-id="d0f14-117">Microsoft Office Communications Server 2007 introduced updated naming for federation types to better define what each federation type actually accomplished:</span></span>

  - <span data-ttu-id="d0f14-118">A Federação aprimorada aberta se tornou conhecida como *domínio de parceiro descoberto*</span><span class="sxs-lookup"><span data-stu-id="d0f14-118">Open Enhanced Federation became known as *Discovered Partner Domain*</span></span>

  - <span data-ttu-id="d0f14-119">A Federação aprimorada se tornou conhecida como *domínio de parceiro permitido*</span><span class="sxs-lookup"><span data-stu-id="d0f14-119">Enhanced Federation became known as *Allowed Partner Domain*</span></span>

  - <span data-ttu-id="d0f14-120">A Federação direta se tornou conhecida como *servidor parceiro permitido*</span><span class="sxs-lookup"><span data-stu-id="d0f14-120">Direct Federation became known as *Allowed Partner Server*</span></span>

  - <span data-ttu-id="d0f14-121">A lista de permissões do servidor se tornou conhecida como *provedor de hospedagem* e provedor de mensagens de chat *públicas*</span><span class="sxs-lookup"><span data-stu-id="d0f14-121">Server Allow List became known as *Hosting Provider* and *Public IM Provider*</span></span>

<span data-ttu-id="d0f14-122">O Microsoft Lync Server 2010 introduziu uma definição mais estreita do provedor de Hospedagem de acordo com o Microsoft Lync Online 2010 e o Microsoft Office 365 e também o fez sujeito à mesma lista permitida definida pelo tipo de Federação do domínio parceiro permitido.</span><span class="sxs-lookup"><span data-stu-id="d0f14-122">Microsoft Lync Server 2010 introduced a narrower definition of Hosting Provider in accordance with Microsoft Lync Online 2010 and Microsoft Office 365 and also made it subject to the same allowed list defined by the Allowed Partner Domain federation type.</span></span>

<span data-ttu-id="d0f14-123">Habilitar a Federação entre o Microsoft Lync Server 2013, o Lync Server 2010 e o Office Communications Server usa os servidores de borda e proxies reverso para impor as regras e os domínios de parceiros permitidos que você definir.</span><span class="sxs-lookup"><span data-stu-id="d0f14-123">Enabling federation between Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server uses the Edge Servers and reverse proxies to enforce the rules and allowed partner domains that you define.</span></span> <span data-ttu-id="d0f14-124">De uma perspectiva de planejamento, a Federação com outro Lync Server, o Office Communications Server exige o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d0f14-124">From a planning perspective, federating with other Lync Server, Office Communications Server requires the following:</span></span>

  - <span data-ttu-id="d0f14-125">Habilite a Federação no construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="d0f14-125">Enable federation in Topology Builder.</span></span> <span data-ttu-id="d0f14-126">Para obter detalhes, consulte o tópico de implantação [Configurando a Federação do SIP, a Federação do XMPP e o sistema de mensagens instantâneas públicas no Lync Server 2013](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="d0f14-126">For details, see the Deployment topic [Configuring SIP federation, XMPP federation and public instant messaging in Lync Server 2013](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md).</span></span>

  - <span data-ttu-id="d0f14-127">Determine suas necessidades para descoberta de domínio federado:</span><span class="sxs-lookup"><span data-stu-id="d0f14-127">Determine your requirements for federated domain discovery:</span></span>
    
      - <span></span>  
        <span data-ttu-id="d0f14-128">Para a configuração manual da Federação, você deve ter o nome de domínio totalmente qualificado (FQDN) do servidor de borda do parceiro e do nome do domínio, ou nome do domínio online, que é inserido no painel de controle do Lync Server, **agrupamento e acesso externo**, **domínios federados do SIP**.</span><span class="sxs-lookup"><span data-stu-id="d0f14-128">For manual configuration of federation, you must have the fully qualified domain name (FQDN) of the partner’s Edge Server and domain name, or online domain name, which is entered in the Lync Server Control Panel, **Federation and External Access**, **SIP Federated Domains**.</span></span> <span data-ttu-id="d0f14-129">Crie uma **nova** política ou **edite** uma política existente para permitir ou bloquear domínios por FQDN.</span><span class="sxs-lookup"><span data-stu-id="d0f14-129">Create a **New** policy or **Edit** an existing policy to either allow or block domains by FQDN.</span></span>
        
        <div>
        

        > [!WARNING]
        > <span data-ttu-id="d0f14-130">A configuração manual do servidor de borda do parceiro de Federação está sujeita a falhas caso o parceiro altere o endereço IP do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="d0f14-130">Manual configuration of a federation partner’s Edge Server is prone to failure in the event that the partner changes the IP address of their Edge Server.</span></span>

        
        </div>
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="d0f14-131">Para <STRONG>novos domínios federados SIP</STRONG>, você deve fornecer o <STRONG>nome de domínio (ou FQDN)</STRONG> para o Microsoft Lync Online e o Microsoft 365 ou o Office 365.</span><span class="sxs-lookup"><span data-stu-id="d0f14-131">For <STRONG>New SIP Federated Domains</STRONG>, you must provide the <STRONG>Domain name (or FQDN)</STRONG> for Microsoft Lync Online and Microsoft 365 or Office 365.</span></span> <span data-ttu-id="d0f14-132">Para o Microsoft Lync Server 2013, Lync Server 2010 e Office Communications Server, você também deve fornecer um <STRONG>serviço de borda de acesso (FQDN)</STRONG></span><span class="sxs-lookup"><span data-stu-id="d0f14-132">For Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server you must also provide an <STRONG>Access Edge service (FQDN)</STRONG></span></span>

        
        </div>
    
      - <span></span>  
        <span data-ttu-id="d0f14-133">Para a Federação de parceiro descoberto, em que os parceiros podem descobrir seu servidor de borda, você cria um registro SRV em seu DNS- \_ sipfederationtls externo. \_ tcp.contoso.com – que aponta para a porta 5061 e para o registro do host (A) de seu servidor de borda</span><span class="sxs-lookup"><span data-stu-id="d0f14-133">For discovered partner federation, where partners can discover your Edge Server, you create an SRV record in your external DNS - \_sipfederationtls.\_tcp.contoso.com – which points to the port 5061 and the host (A) record of your Edge Server</span></span>
        
        <div>
        

        > [!IMPORTANT]
        > <span data-ttu-id="d0f14-134">Se você estiver oferecendo suporte para clientes móveis do Microsoft Lync no Windows Phone ou no iPhone do Apple, no iPad ou em outros dispositivos Apple e estiver usando o serviço de notificação por Push ou o serviço de notificação por push, você deve planejar o sipfederationtls. _ TCP.</span><span class="sxs-lookup"><span data-stu-id="d0f14-134">If you are supporting Microsoft Lync Mobile clients on either Windows Phone or Apple iPhone, iPad, or other Apple devices and are using the Push Notification Service or Push Notification Service, you must plan for _sipfederationtls._tcp.</span></span> <span data-ttu-id="d0f14-135">&lt;&gt;Registros SRV do domínio SIP para cada domínio SIP para os quais você tem clientes móveis do Lync.</span><span class="sxs-lookup"><span data-stu-id="d0f14-135">&lt;SIP domain&gt; SRV records for each SIP domain that you have Lync Mobile clients.</span></span> <span data-ttu-id="d0f14-136">Android e Nokia Symbian Lync Mobile não use a notificação por push e não está sujeito a esse requisito.</span><span class="sxs-lookup"><span data-stu-id="d0f14-136">Android and Nokia Symbian Lync Mobile do not use push notification and are not subject to this requirement.</span></span>

        
        </div>

  - <span data-ttu-id="d0f14-137">Configurar políticas de acesso de usuários externos para dar suporte a domínios federados</span><span class="sxs-lookup"><span data-stu-id="d0f14-137">Configure external user access policies to support federated domains</span></span>

  - <span data-ttu-id="d0f14-138">Abra portas de firewall para o protocolo SIP, conferência da Web e áudio/visual para acomodar a Federação ou os contatos que você está habilitando.</span><span class="sxs-lookup"><span data-stu-id="d0f14-138">Open firewall ports for session initiation protocol (SIP), web conferencing and audio/visual to accommodate the federation or contacts that you are enabling.</span></span> <span data-ttu-id="d0f14-139">Para obter detalhes, consulte: [determinar requisitos de firewall e porta externo A/V para o Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="d0f14-139">For details, see: [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)</span></span>

<span data-ttu-id="d0f14-140">As informações a seguir ajudarão você a definir os requisitos de certificado, de porta/protocolo e DNS para federação com o Microsoft Lync Server 2013 e o Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d0f14-140">The following information will aid you in defining the certificate, port/protocol and DNS requirements for federation with Microsoft Lync Server 2013 and Lync Server 2010.</span></span>

<span data-ttu-id="d0f14-141">O planejamento de certificados, firewall e requisitos de porta/protocolo e requisitos de DNS geralmente é um processo direto se você planejou ou implantou seus servidores de borda do Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d0f14-141">Planning for certificates, firewall and port/protocol requirements and DNS requirements is generally a straight forward process if you have planned or deployed your Microsoft Lync Server 2013 Edge Servers.</span></span> <span data-ttu-id="d0f14-142">Como a Federação é um recurso adicional que usa o servidor de borda existente, os requisitos de planejamento geralmente são atendidos pelo planejamento e implantação do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="d0f14-142">Because federation is an additional feature that uses the existing Edge Server, the planning requirements are generally met by the Edge Server planning and deployment.</span></span> <span data-ttu-id="d0f14-143">Você deve usar as tabelas a seguir para determinar se os seus requisitos são atendidos e fazer alterações de acordo com a porta/protocolo e DNS.</span><span class="sxs-lookup"><span data-stu-id="d0f14-143">You should use the following tables to determine that your requirements are met and make changes in port/protocol and DNS accordingly.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="d0f14-144">Se você tiver um pool de servidores de borda e estiver conferindo-se com os parceiros do Lync Server 2013 ou Lync Server 2010, poderá usar o balanceamento de carga DNS ou os balanceadores de carga de hardware nos lados internos e externos dos servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="d0f14-144">If you have a pool of Edge Servers and are federating with Lync Server 2013 or Lync Server 2010 partners, then you can use either DNS load balancing or hardware load balancers on the internal and external facing sides of the Edge Servers.</span></span> <span data-ttu-id="d0f14-145">Se você estiver fazendo a Federação com o Office Communications Server 2007 ou o Office Communications Server 2007 R2, o balanceamento de carga de hardware fornecerá suporte de failover em caso de um servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="d0f14-145">If you are federating with Office Communications Server 2007 or Office Communications Server 2007 R2, hardware load balancing will provide failover support in the event of an Edge Server.</span></span> <span data-ttu-id="d0f14-146">O Office Communications Server 2007 e o Office Communications Server 2007 R2 não têm reconhecimento de balanceamento de carga de DNS.</span><span class="sxs-lookup"><span data-stu-id="d0f14-146">Office Communications Server 2007 and Office Communications Server 2007 R2 are not DNS load balancing aware.</span></span> <span data-ttu-id="d0f14-147">Os servidores de borda de parceiro estabelecerão comunicação com o primeiro servidor de borda no pool que responde.</span><span class="sxs-lookup"><span data-stu-id="d0f14-147">The partner Edge Servers will establish communication with the first Edge Server in your pool that responds.</span></span> <span data-ttu-id="d0f14-148">Se esse servidor de borda falhar, a comunicação não executará automaticamente o failover.</span><span class="sxs-lookup"><span data-stu-id="d0f14-148">If that Edge Server fails, communication does not automatically failover.</span></span>



</div>

<span data-ttu-id="d0f14-149">Os requisitos do certificado geralmente são atendidos pelo planejamento de certificados para o servidor de borda escolhido ou plano do servidor de borda em pool.</span><span class="sxs-lookup"><span data-stu-id="d0f14-149">Certificate requirements are typically met through the planning of certificates for your chosen Edge Server or pooled Edge Server plan.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d0f14-150">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d0f14-150">In This Section</span></span>

  - [<span data-ttu-id="d0f14-151">Resumo do certificado-SIP, Federação do XMPP e mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f14-151">Certificate summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-sip-xmpp-federation-and-public-instant-messaging.md)

  - [<span data-ttu-id="d0f14-152">Resumo da porta-SIP, Federação do XMPP e mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f14-152">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-port-summary-sip-xmpp-federation-and-public-instant-messaging.md)

  - [<span data-ttu-id="d0f14-153">Resumo de DNS-SIP, Federação de XMPP e mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f14-153">DNS summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-dns-summary-sip-xmpp-federation-and-public-instant-messaging.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d0f14-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0f14-154">See Also</span></span>


[<span data-ttu-id="d0f14-155">Configurar políticas para controlar acesso de usuário federado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f14-155">Configure policies to control federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-federated-user-access.md)  


[<span data-ttu-id="d0f14-156">Cenários de acesso de usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f14-156">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="d0f14-157">Determinar firewall A/V externo e requisitos de porta para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f14-157">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
[<span data-ttu-id="d0f14-158">Determinar requisitios de DNS para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f14-158">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="d0f14-159">Gerenciar configuração da borda de acesso para sua organização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f14-159">Manage Access Edge Configuration for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-access-edge-configuration-for-your-organization.md)  
[<span data-ttu-id="d0f14-160">Gerenciar domínios SIP federados para sua organização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f14-160">Manage SIP federated domains for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)  
[<span data-ttu-id="d0f14-161">Gerenciar fornecedores SIP federados para sua organização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f14-161">Manage SIP federated providers for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-providers-for-your-organization.md)  
  

<span data-ttu-id="d0f14-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d0f14-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

