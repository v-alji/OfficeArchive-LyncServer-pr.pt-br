---
title: 'Lync Server 2013: Configuração de federação do Lync'
description: 'Lync Server 2013: Configurando a federação do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390326"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a><span data-ttu-id="a84cc-103">Configuração de federação do Lync no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a84cc-103">Setting up Lync federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a84cc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a84cc-104">

<span> </span></span></span>

<span data-ttu-id="a84cc-105">_**Tópico Última Modificação:** 2014-03-27_</span><span class="sxs-lookup"><span data-stu-id="a84cc-105">_**Topic Last Modified:** 2014-03-27_</span></span>

<span data-ttu-id="a84cc-106">Se você já tiver implantado servidores ou servidores de Borda, a adição dos recursos de cenários federados será direta.</span><span class="sxs-lookup"><span data-stu-id="a84cc-106">If you have already deployed you Edge server or servers, adding the federated scenarios features is straight forward.</span></span> <span data-ttu-id="a84cc-107">Se você não tiver configurar Servidores de Borda, deverá fazer isso primeiro.</span><span class="sxs-lookup"><span data-stu-id="a84cc-107">If you have not set up Edge Servers, you must do that first.</span></span> <span data-ttu-id="a84cc-108">Para obter detalhes, consulte: Planning for external [user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span><span class="sxs-lookup"><span data-stu-id="a84cc-108">For details, see: [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a84cc-109">Se você pretende configurar qualquer combinação de federação XMPP, Federação do Lync ou conectividade de mensagens instantâneas públicas, poderá implantá-las simultaneamente ou uma de cada vez.</span><span class="sxs-lookup"><span data-stu-id="a84cc-109">If you intend to setup any combination of XMPP federation, Lync Federation, or public instant messaging connectivity, you can deploy them concurrently or one at a time.</span></span> <span data-ttu-id="a84cc-110">Se você configurar as opções por meio do Construtor de Topologias e do shell de Gerenciamento do Lync Server, execute o Assistente de Implantação no servidor de Borda depois de configurar as opções para um, dois ou todos os três tipos de federação, você poderá reduzir o número de etapas necessárias.</span><span class="sxs-lookup"><span data-stu-id="a84cc-110">If you configure the options through the Topology Builder and the Lync Server Management shell, then run the Deployment Wizard at the Edge server after configuring the options for one, two or all three federation types, you can reduce the number of steps required.</span></span>



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a><span data-ttu-id="a84cc-111">Configurando a Federação do Lync no Construtor de Topologias e no Assistente de Implantação</span><span class="sxs-lookup"><span data-stu-id="a84cc-111">Setting Up Lync Federation in Topology Builder and the Deployment Wizard</span></span>

1.  <span data-ttu-id="a84cc-112">Em um servidor Front-End, abra o Construtor de Topologias.</span><span class="sxs-lookup"><span data-stu-id="a84cc-112">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="a84cc-113">Expanda pools de borda e clique com o botão direito do mouse em seu servidor de Borda ou pool de servidores de Borda.</span><span class="sxs-lookup"><span data-stu-id="a84cc-113">Expand Edge pools, then right click your Edge server or Edge server pool.</span></span> <span data-ttu-id="a84cc-114">Selecione Editar propriedades.</span><span class="sxs-lookup"><span data-stu-id="a84cc-114">Select Edit properties.</span></span>

2.  <span data-ttu-id="a84cc-115">Em Editar Propriedades em Geral, selecione Habilitar federação para este pool de Borda (Porta 5061).</span><span class="sxs-lookup"><span data-stu-id="a84cc-115">In Edit Properties under General, select Enable federation for this Edge pool (Port 5061).</span></span> <span data-ttu-id="a84cc-116">Clique em OK.</span><span class="sxs-lookup"><span data-stu-id="a84cc-116">Click OK.</span></span>

3.  <span data-ttu-id="a84cc-117">Clique em Ação, selecione Topologia, selecione Publicar.</span><span class="sxs-lookup"><span data-stu-id="a84cc-117">Click Action, select Topology, select Publish.</span></span> <span data-ttu-id="a84cc-118">Quando solicitado em Publicar a topologia, clique em Next.</span><span class="sxs-lookup"><span data-stu-id="a84cc-118">When prompted on Publish the topology, click Next.</span></span> <span data-ttu-id="a84cc-119">Quando a Publicação for concluída, clique em Concluir.</span><span class="sxs-lookup"><span data-stu-id="a84cc-119">When the Publish is finished, click Finish.</span></span>

4.  <span data-ttu-id="a84cc-120">No servidor de Borda, abra o assistente de Implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a84cc-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="a84cc-121">Clique em Instalar ou Atualizar o Sistema do Lync Server e clique em Configurar ou Remover Componentes do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="a84cc-121">Click Install or Update Lync Server System, then click Setup or Remove Lync Server Components.</span></span> <span data-ttu-id="a84cc-122">Clique em Executar Novamente.</span><span class="sxs-lookup"><span data-stu-id="a84cc-122">Click Run Again.</span></span>

5.  <span data-ttu-id="a84cc-123">Em Configurar componentes do Lync Server, clique em Próximo.</span><span class="sxs-lookup"><span data-stu-id="a84cc-123">At Setup Lync Server components, click Next.</span></span> <span data-ttu-id="a84cc-124">A tela de resumo mostrará as ações à medida que elas são executadas.</span><span class="sxs-lookup"><span data-stu-id="a84cc-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="a84cc-125">Depois que a implantação for feita, clique em Exibir Log para exibir arquivos de log disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a84cc-125">Once the deployment is done, click View Log to view available log files.</span></span> <span data-ttu-id="a84cc-126">Clique em Concluir para concluir a implantação.</span><span class="sxs-lookup"><span data-stu-id="a84cc-126">Click Finish to complete the deployment.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="a84cc-127">Você pode selecionar essa opção, mas apenas um pool de Borda ou Servidor de Borda em sua organização pode ser publicado externamente para federação.</span><span class="sxs-lookup"><span data-stu-id="a84cc-127">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="a84cc-128">Todos os acessos por usuários federados, incluindo usuários de mensagens instantâneas públicas (IM), passam pelo mesmo pool de Borda ou servidor de borda único.</span><span class="sxs-lookup"><span data-stu-id="a84cc-128">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="a84cc-129">Por exemplo, se sua implantação incluir um pool de Borda ou um único Servidor de Borda implantado em Nova York e um implantado em Londres e você habilitar o suporte de federação no pool de Borda de Nova York ou servidor de borda único, o tráfego de sinal para usuários federados passará pelo pool de Borda de Nova York ou pelo servidor de borda único.</span><span class="sxs-lookup"><span data-stu-id="a84cc-129">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="a84cc-130">Isso se aplica inclusive para comunicações com usuários de Londres, embora um usuário interno de Londres chamando um usuário federado de Londres use o pool de Londres ou Servidor de Borda para tráfego de A/V.</span><span class="sxs-lookup"><span data-stu-id="a84cc-130">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a><span data-ttu-id="a84cc-131">Configurando Federação com Parceiros</span><span class="sxs-lookup"><span data-stu-id="a84cc-131">Configuring Federation with Partners</span></span>

1.  <span data-ttu-id="a84cc-132">Para configurar uma federação bem-sucedida com outro Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2 ou Office Communicator 2007, selecione o tipo de federação na tabela a seguir e defina registros SRV DNS, host DNS (A ou AAAA para IPv6) e configure políticas aplicáveis ao tipo de federação:</span><span class="sxs-lookup"><span data-stu-id="a84cc-132">To setup a successful federation with another Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2, or Office Communicator 2007, select the type of federation from the following table and define DNS SRV records, DNS host (A or AAAA for IPv6) and configure policies applicable to the type of federation:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="a84cc-133">Tipo de federação</span><span class="sxs-lookup"><span data-stu-id="a84cc-133">Federation type</span></span></th>
    <th><span data-ttu-id="a84cc-134">Registros DNS</span><span class="sxs-lookup"><span data-stu-id="a84cc-134">DNS Records</span></span></th>
    <th><span data-ttu-id="a84cc-135">Definição de Política</span><span class="sxs-lookup"><span data-stu-id="a84cc-135">Policy Definition</span></span></th>
    <th><span data-ttu-id="a84cc-136">Observações</span><span class="sxs-lookup"><span data-stu-id="a84cc-136">Notes</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="a84cc-137">Domínio do Parceiro Descoberto</span><span class="sxs-lookup"><span data-stu-id="a84cc-137">Discovered Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="a84cc-138">Configure o registro SRV do formato _sipfederationtls._tcp. &lt; nome de domínio externo Onde o valor da porta para o registro SRV é &gt; TCP 5061 e o <strong>Host que</strong> oferece esse serviço é definido como sip.</span><span class="sxs-lookup"><span data-stu-id="a84cc-138">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="a84cc-139">&lt;nome de domínio &gt; externo – o FQDN do seu serviço de Borda de Acesso.</span><span class="sxs-lookup"><span data-stu-id="a84cc-139">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="a84cc-140">Consulte <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> para obter detalhes sobre como criar o registro SRV</span><span class="sxs-lookup"><span data-stu-id="a84cc-140">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="a84cc-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar ou desabilitar federação e conectividade de IM pública no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a84cc-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="a84cc-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Habilitar ou desabilitar descoberta de parceiros de federação no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a84cc-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Enable or disable discovery of federation partners in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="a84cc-143">As versões anteriores se referiam a esse tipo de federação como <strong>Federação Aprimorada Aberta.</strong></span><span class="sxs-lookup"><span data-stu-id="a84cc-143">Previous versions referred to this type of federation as <strong>Open Enhanced Federation</strong>.</span></span> <span data-ttu-id="a84cc-144">A criação do registro SRV é necessária para esse tipo de federação e é permitir que outros parceiros descubram sua federação.</span><span class="sxs-lookup"><span data-stu-id="a84cc-144">The creation of the SRV record is required for this type of federation and is to allow other partners to discover your federation.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="a84cc-145">Domínio de parceiro permitido</span><span class="sxs-lookup"><span data-stu-id="a84cc-145">Allowed Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="a84cc-146">Configure o registro SRV do formato _sipfederationtls._tcp. &lt; nome de domínio externo Onde o valor da porta para o registro SRV é &gt; TCP 5061 e o <strong>Host que</strong> oferece esse serviço é definido como sip.</span><span class="sxs-lookup"><span data-stu-id="a84cc-146">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="a84cc-147">&lt;nome de domínio &gt; externo – o FQDN do seu serviço de Borda de Acesso.</span><span class="sxs-lookup"><span data-stu-id="a84cc-147">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="a84cc-148">Consulte <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> para obter detalhes sobre como criar o registro SRV</span><span class="sxs-lookup"><span data-stu-id="a84cc-148">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="a84cc-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar ou desabilitar federação e conectividade de IM pública no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a84cc-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="a84cc-150">As versões anteriores se referiam a esse tipo de federação como <strong>Federação Aprimorada.</strong></span><span class="sxs-lookup"><span data-stu-id="a84cc-150">Previous versions referred to this type of federation as <strong>Enhanced Federation</strong>.</span></span> <span data-ttu-id="a84cc-151">A criação do registro SRV é opcional para esse tipo de federação e é permitir que outros parceiros descubram sua federação.</span><span class="sxs-lookup"><span data-stu-id="a84cc-151">The creation of the SRV record is optional for this type of federation and is to allow other partners to discover your federation.</span></span> <span data-ttu-id="a84cc-152">É claro que, em seguida, isso é <strong>uma Federação Aprimorada Aberta</strong>ou Domínio do Parceiro <strong>Descoberto</strong></span><span class="sxs-lookup"><span data-stu-id="a84cc-152">Of course, this is then an <strong>Open Enhanced Federation</strong>, or <strong>Discovered Partner Domain</strong></span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="a84cc-153">Servidor parceiro permitido</span><span class="sxs-lookup"><span data-stu-id="a84cc-153">Allowed Partner Server</span></span></p></td>
    <td><p><span data-ttu-id="a84cc-154">Configurar o nome de domínio SIP e o FQDN do servidor de borda parceiro como um parceiro de federação em Políticas</span><span class="sxs-lookup"><span data-stu-id="a84cc-154">Configure the SIP domain name and the partner Edge Server FQDN as a federation partner in Policies</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="a84cc-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar ou desabilitar federação e conectividade de IM pública no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a84cc-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="a84cc-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configurar suprote para domínios externos permitidos no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a84cc-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configure support for allowed external domains in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="a84cc-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configurar suporte para domínios externos bloqueados no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a84cc-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configure support for blocked external domains in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="a84cc-158">Esse tipo de federação é a definição de um para um relacionamento e não permite a descoberta de outros parceiros de federação.</span><span class="sxs-lookup"><span data-stu-id="a84cc-158">This federation type is the definition of a one to one relationship and does not allow for discovery of other federation partners.</span></span> <span data-ttu-id="a84cc-159">Cada parceiro de federação é configurado explicitamente.</span><span class="sxs-lookup"><span data-stu-id="a84cc-159">Each federation partner is configured explicitly.</span></span> <span data-ttu-id="a84cc-160">Nas versões anteriores, isso era conhecido como <strong>Federação Direta</strong></span><span class="sxs-lookup"><span data-stu-id="a84cc-160">In previous versions, this was known as <strong>Direct Federation</strong></span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="a84cc-161">Provedor de Hospedagem e Provedor público de IM</span><span class="sxs-lookup"><span data-stu-id="a84cc-161">Hosting Provider and Public IM Provider</span></span></p></td>
    <td><p><span data-ttu-id="a84cc-162">Nenhum requisito DNS específico é definido para esse tipo de federação</span><span class="sxs-lookup"><span data-stu-id="a84cc-162">No specific DNS requirements are defined for this type of federation</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="a84cc-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Habilitar ou desabilitar federação e conectividade de IM pública no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a84cc-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="a84cc-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Criar ou editar fornecedores SIP públicos federados no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a84cc-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Create or edit public SIP federated providers in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="a84cc-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Criar ou editar provedores hospedados federados SIP no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="a84cc-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Create or edit hosted SIP federated providers Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="a84cc-166">Esse tipo de federação define serviços e provedores de hospedagem que você deseja configurar para seus usuários.</span><span class="sxs-lookup"><span data-stu-id="a84cc-166">This federation type defines services and hosting providers that you want to configure for your users.</span></span> <span data-ttu-id="a84cc-167">Os usos típicos incluem configuração para provedores públicos de IM, como Windows Live Messenger, Yahoo!</span><span class="sxs-lookup"><span data-stu-id="a84cc-167">Typical uses include configuration for public IM providers like Windows Live Messenger, Yahoo!</span></span> <span data-ttu-id="a84cc-168">e AOL, bem como provedores de hospedagem como o Lync Online e o Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a84cc-168">and AOL, as well as hosting providers such as Lync Online and Microsoft 365</span></span></p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="a84cc-169">A partir de 1º de setembro de 2012, a Licença de Assinatura do Usuário de Conectividade pública de IM do Microsoft Lync ("PIC USL") não está mais disponível para compra para contratos novos ou renovadores.</span><span class="sxs-lookup"><span data-stu-id="a84cc-169">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="a84cc-170">Os clientes com licenças ativas poderão continuar federados com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="a84cc-170">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="a84cc-171">Messenger até a data de encerrar o serviço.</span><span class="sxs-lookup"><span data-stu-id="a84cc-171">Messenger until the service shut down date.</span></span> <span data-ttu-id="a84cc-172">Uma data de fim de vida de junho de 2014 para AOL e Yahoo!</span><span class="sxs-lookup"><span data-stu-id="a84cc-172">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="a84cc-173">foi anunciado.</span><span class="sxs-lookup"><span data-stu-id="a84cc-173">has been announced.</span></span> <span data-ttu-id="a84cc-174">Para obter detalhes, <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">consulte Support for public instant messenger connectivity in Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a84cc-174">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="a84cc-175">A USL pic é uma licença de assinatura por usuário por mês que é necessária para o Lync Server ou o Office Communications Server federar com o Yahoo!</span><span class="sxs-lookup"><span data-stu-id="a84cc-175">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="a84cc-176">Messenger.</span><span class="sxs-lookup"><span data-stu-id="a84cc-176">Messenger.</span></span> <span data-ttu-id="a84cc-177">A capacidade da Microsoft de fornecer esse serviço foi contingente com o suporte do Yahoo!, o contrato subjacente para o qual está se esvaindo.</span><span class="sxs-lookup"><span data-stu-id="a84cc-177">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="a84cc-178">Mais do que nunca, o Lync é uma ferramenta poderosa para se conectar entre organizações e com indivíduos em todo o mundo.</span><span class="sxs-lookup"><span data-stu-id="a84cc-178">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="a84cc-179">A federação Windows Live Messenger requer licenças de usuário/dispositivo adicionais além da CAL padrão do Lync.</span><span class="sxs-lookup"><span data-stu-id="a84cc-179">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="a84cc-180">A federação do Skype será adicionada a essa lista, permitindo que os usuários do Lync alcancem centenas de milhões de pessoas com mensagens de IM e voz.</span><span class="sxs-lookup"><span data-stu-id="a84cc-180">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  <span data-ttu-id="a84cc-181">Definir e configurar qualquer host DNS necessário (A ou AAAA para IPv6) e registros SRV DNS</span><span class="sxs-lookup"><span data-stu-id="a84cc-181">Define and configure any required DNS host (A or AAAA for IPv6) and DNS SRV records</span></span>

3.  <span data-ttu-id="a84cc-182">Defina e configure todas as políticas usando o Painel de Controle do Lync Server ou usando o Shell de Gerenciamento do Lync Server e os cmdlets apropriados.</span><span class="sxs-lookup"><span data-stu-id="a84cc-182">Define and configure any policies using the Lync Server Control Panel or by using the Lync Server Management Shell and the appropriate cmdlets.</span></span> <span data-ttu-id="a84cc-183">Para obter detalhes sobre os cmdlets do Shell de Gerenciamento do Lync Server, consulte [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)</span><span class="sxs-lookup"><span data-stu-id="a84cc-183">For details on the Lync Server Management Shell cmdlets, see [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a84cc-184">O Lync Room System (LRS) não mostra o botão de junção para reuniões enviadas pelos organizadores em parceiros federados do Lync.</span><span class="sxs-lookup"><span data-stu-id="a84cc-184">Lync Room System (LRS) does not show join button for meetings sent by organizers in federated Lync partners.</span></span> <span data-ttu-id="a84cc-185">Para que um link de junção de reunião apareça no LRS, a organização de envio deve habilitar o TNEF usando o seguinte cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a84cc-185">For a meeting join link to appear on LRS, the sending organization must enable TNEF by using the following cmdlet:</span></span><BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR><span data-ttu-id="a84cc-186">Observe que isso não é específico do LRS.</span><span class="sxs-lookup"><span data-stu-id="a84cc-186">Note that this is not LRS specific.</span></span> <span data-ttu-id="a84cc-187">O Outlook e o Lync também não mostrariam Links de junção neste caso, pois as propriedades MAPI não são transportadas, mas, no caso do Outlook, o usuário pode abrir o convite da reunião e clicar na URL da reunião.</span><span class="sxs-lookup"><span data-stu-id="a84cc-187">Outlook and Lync would also not show Join links in this case as MAPI properties are not transported, but in the Outlook case, the user can open up the meeting invite and click on the meeting URL.</span></span> <span data-ttu-id="a84cc-188">Quando O TNEFEnabled é definido como verdadeiro, o Exchange 2013 não tira propriedades MAPI, incluindo OnlineMeetingExternalLink e o botão Ingressar será mostrado no lembrete.</span><span class="sxs-lookup"><span data-stu-id="a84cc-188">When TNEFEnabled is set to true Exchange 2013 does not strip MAPI properties including OnlineMeetingExternalLink and the Join button will be shown on the reminder.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a84cc-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="a84cc-189">See Also</span></span>


[<span data-ttu-id="a84cc-190">Planejamento para SIP, federação XMPP e mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a84cc-190">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[<span data-ttu-id="a84cc-191">Gerenciamento de federação e acesso externo ao Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a84cc-191">Managing federation and external access to Lync Server 2013</span></span>](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

<span data-ttu-id="a84cc-192"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a84cc-192"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

