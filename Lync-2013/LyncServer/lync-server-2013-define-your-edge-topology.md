---
title: 'Lync Server 2013: definir sua topologia de borda'
description: 'Lync Server 2013: definir sua topologia de borda.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define your edge topology
ms:assetid: 787b23f1-8fa0-4c37-abf2-c516c5dd66f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398591(v=OCS.15)
ms:contentKeyID: 48184562
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd4aa16ca23d24f0edd92189216030ef926fc841
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431033"
---
# <a name="define-your-edge-topology-in-lync-server-2013"></a><span data-ttu-id="8e622-103">Definir sua topologia de borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e622-103">Define your edge topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e622-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e622-104">

<span> </span></span></span>

<span data-ttu-id="8e622-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="8e622-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="8e622-106">Você deve usar o construtor de topologias para criar sua topologia e deve configurar pelo menos um pool de front-end interno ou um servidor Standard Edition para poder implantar o servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-106">You must use Topology Builder to build your topology and you must set up at least one internal Front End pool or Standard Edition server before you can deploy your Edge Server.</span></span> <span data-ttu-id="8e622-107">Use o procedimento a seguir para definir a topologia de borda para um único servidor de borda e, em seguida, use os procedimentos em [publicar sua topologia no Lync server 2013](lync-server-2013-publish-your-topology.md) e [exportar sua topologia do Lync Server 2013 e copiá-la para a mídia externa para a instalação do Edge](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) para publicar a topologia e disponibilizá-la para o servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-107">Use the following procedure to define the edge topology for a single Edge Server, and then use the procedures in [Publish your topology in Lync Server 2013](lync-server-2013-publish-your-topology.md) and [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) to publish the topology and make it available to your Edge Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8e622-108">As interfaces de Borda interna e externa precisam usar o mesmo tipo de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="8e622-108">The internal Edge interface and external Edge interface must use the same type of load balancing.</span></span> <span data-ttu-id="8e622-109">Não é possível usar balanceamento de carga DNS em uma interface de Borda e balanceamento de carga de hardware na outra interface de Borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-109">You cannot use DNS load balancing on one Edge interface and hardware load balancing on the other Edge interface.</span></span>



</div>

<span data-ttu-id="8e622-110">Para publicar, habilitar ou desabilitar uma topologia com êxito ao adicionar ou remover uma função de servidor, você deve estar conectado como um usuário que é membro do grupo RTCUniversalServerAdmins e administradores do domínio.</span><span class="sxs-lookup"><span data-stu-id="8e622-110">To successfully publish, enable, or disable a topology when adding or removing a server role, you must be logged in as a user who is a member of the RTCUniversalServerAdmins and Domain Admins groups.</span></span> <span data-ttu-id="8e622-111">Você também pode conceder direitos e permissões de administrador necessários para adicionar funções de servidor a uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="8e622-111">You can also grant the administrator rights and permissions required for adding server roles to a user account.</span></span> <span data-ttu-id="8e622-112">Para obter detalhes, consulte [delegar permissões de configuração no Lync Server 2013](lync-server-2013-delegate-setup-permissions.md) na documentação de implantação do servidor Standard Edition ou Enterprise Edition Server.</span><span class="sxs-lookup"><span data-stu-id="8e622-112">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md) in the Standard Edition server or Enterprise Edition server Deployment documentation.</span></span> <span data-ttu-id="8e622-113">Para outras alterações de configuração, somente a associação no grupo RTCUniversalServerAdmins é necessária.</span><span class="sxs-lookup"><span data-stu-id="8e622-113">For other configuration changes, only membership in the RTCUniversalServerAdmins group is required.</span></span>

<span data-ttu-id="8e622-114">Se você definiu a topologia de borda quando definiu e publicou sua topologia interna, e nenhuma alteração é necessária para a topologia de borda que você definiu anteriormente, você não precisa defini-la e publicá-la novamente.</span><span class="sxs-lookup"><span data-stu-id="8e622-114">If you defined your edge topology when you defined and published your internal topology, and no changes are required to the edge topology that you previously defined, you do not need to do define it and publish it again.</span></span> <span data-ttu-id="8e622-115">Use o procedimento a seguir somente se precisar fazer alterações na sua topologia de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-115">Use the following procedure only if you need to make changes to your edge topology.</span></span> <span data-ttu-id="8e622-116">Você deve disponibilizar a topologia previamente definida e publicada para seus servidores de borda, usando o procedimento em [exportar sua topologia do Lync Server 2013 e copiá-la para a mídia externa para instalação do Edge](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span><span class="sxs-lookup"><span data-stu-id="8e622-116">You must make the previously defined and published topology available to your Edge Servers, which you do by using the procedure in [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="8e622-117">Não é possível executar o construtor de topologias a partir de um servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-117">You cannot run Topology Builder from an Edge Server.</span></span> <span data-ttu-id="8e622-118">Você deve executá-lo a partir de seu servidor front-end ou servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="8e622-118">You must run it from your Front End Server or Standard Edition servers.</span></span>



</div>

<span data-ttu-id="8e622-119">O processo para definir a topologia do servidor de borda é feito no construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="8e622-119">The process to define your Edge Server topology is done in Topology Builder.</span></span> <span data-ttu-id="8e622-120">Os três tipos principais de topologias de servidor de borda que você planeja e configura estão listados abaixo:</span><span class="sxs-lookup"><span data-stu-id="8e622-120">The three primary types of Edge Server topologies that you plan and configure are listed below:</span></span>

  - <span data-ttu-id="8e622-121">Para definir a topologia para um servidor de borda único</span><span class="sxs-lookup"><span data-stu-id="8e622-121">To define the Topology for a Single Edge Server</span></span>

  - <span data-ttu-id="8e622-122">Para definir a topologia de um pool de servidores de borda com balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="8e622-122">To define the Topology for a Load Balanced Edge Server Pool</span></span>

  - <span data-ttu-id="8e622-123">Para definir a topologia de um pool de bordas com carga balanceada de hardware</span><span class="sxs-lookup"><span data-stu-id="8e622-123">To define the Topology for a Hardware Load Balanced Edge Pool</span></span>

<div>

## <a name="to-define-the-topology-for-a-single-edge-server"></a><span data-ttu-id="8e622-124">Para definir a topologia para um servidor de borda único</span><span class="sxs-lookup"><span data-stu-id="8e622-124">To define the topology for a single Edge Server</span></span>

1.  <span data-ttu-id="8e622-125">Iniciar o construtor de topologias: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Construtor de topologias do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="8e622-125">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="8e622-126">Na árvore de console, expanda o site no qual você deseja implantar um servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-126">In the console tree, expand the site in which you want to deploy an Edge Server.</span></span>

3.  <span data-ttu-id="8e622-127">Clique com o botão direito do mouse em **conjuntos de bordas** e clique em **novo pool de bordas**.</span><span class="sxs-lookup"><span data-stu-id="8e622-127">Right-click **Edge pools**, and then click **New Edge Pool**.</span></span>

4.  <span data-ttu-id="8e622-128">Em **definir o novo pool de bordas**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-128">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="8e622-129">Em **definir o FQDN do pool de bordas**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-129">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-130">Em **pool FQDN**, digite o nome de domínio totalmente qualificado (FQDN) da interface interna do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-130">In **Pool FQDN**, type the fully qualified domain name (FQDN) of the internal interface for the Edge Server.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="8e622-131">O nome que você especificar dever ser idêntico ao nome de computador configurado no servidor.</span><span class="sxs-lookup"><span data-stu-id="8e622-131">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="8e622-132">Por padrão, o nome do computador de um computador que não está associado a um domínio é um nome curto, e não um FQDN.</span><span class="sxs-lookup"><span data-stu-id="8e622-132">By default the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="8e622-133">O Construtor de Topologias usa FQDNs, não nomes curtos.</span><span class="sxs-lookup"><span data-stu-id="8e622-133">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="8e622-134">Portanto, você deverá configurar um sufixo DNS no nome do computador a ser implantado no Servidor de Borda que não ingressou no domínio.</span><span class="sxs-lookup"><span data-stu-id="8e622-134">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="8e622-135">Use apenas caracteres padrão (incluindo A–Z, a–z, 0–9 e hifens) ao atribuir FQDNs de seus Lync Servers, Servidores de Borda e pools.</span><span class="sxs-lookup"><span data-stu-id="8e622-135">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="8e622-136">Não use caracteres Unicode ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="8e622-136">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="8e622-137">Os caracteres não padrão em um FQDN geralmente não são compatíveis com o DNS externo e CAs públicas (quando o FQDN deve ser atribuído ao SN no certificado).</span><span class="sxs-lookup"><span data-stu-id="8e622-137">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="8e622-138">Para obter detalhes sobre como adicionar um sufixo DNS a um nome de computador, consulte <A href="lync-server-2013-configure-dns-for-edge-support.md">Configurar o DNS para suporte de borda no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="8e622-138">For details about adding a DNS suffix to a computer name, see <A href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</A>.</span></span>

        
        </div>
    
      - <span data-ttu-id="8e622-139">Clique em **pool de computador único** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-139">Click **Single computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="8e622-140">Em **selecionar recursos**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-140">In **Select features**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-141">Se você pretende usar um único FQDN e um único endereço IP para o serviço de acesso SIP, serviço de Webconferência do Lync Server 2013 e os/V Edge Services, marque a caixa de seleção **usar um único FQDN e endereço IP** .</span><span class="sxs-lookup"><span data-stu-id="8e622-141">If you plan to use a single FQDN and IP address for the SIP Access service, Lync Server 2013 Web Conferencing service, and A/V Edge services, select the **Use a single FQDN and IP Address** check box.</span></span>
    
      - <span data-ttu-id="8e622-142">Se você planeja habilitar a Federação, marque a caixa de seleção **habilitar Federação para este pool de bordas (porta 5061)** .</span><span class="sxs-lookup"><span data-stu-id="8e622-142">If you plan to enable federation select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8e622-143">Você pode selecionar essa opção, mas somente um pool de bordas ou um servidor de borda em sua organização pode ser publicado externamente para Federação.</span><span class="sxs-lookup"><span data-stu-id="8e622-143">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="8e622-144">Todo o acesso de usuários federados, incluindo usuários públicos de mensagens instantâneas (IM), passam pelo mesmo pool de bordas ou servidor de borda única.</span><span class="sxs-lookup"><span data-stu-id="8e622-144">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="8e622-145">Por exemplo, se sua implantação inclui um pool de bordas ou um servidor de borda única implantado em Nova York e um implantado em Londres e você habilitar o suporte de Federação no pool de bordas de Nova York ou no servidor de borda único, o tráfego de sinal para usuários federados passará pelo novo grupo de bordas de Iorque ou pelo servidor de borda única.</span><span class="sxs-lookup"><span data-stu-id="8e622-145">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="8e622-146">Isso se aplica inclusive para comunicações com usuários de Londres, embora um usuário interno de Londres chamando um usuário federado de Londres use o pool de Londres ou Servidor de Borda para tráfego de A/V.</span><span class="sxs-lookup"><span data-stu-id="8e622-146">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="8e622-147">Se você planeja dar suporte ao protocolo de mensagens extensíveis e presença (XMPP) para a sua implantação, marque a caixa de seleção **habilitar Federação de XMPP (porta 5269)**</span><span class="sxs-lookup"><span data-stu-id="8e622-147">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="8e622-148">Em **selecionar opções de IP**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-148">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-149">**Habilitar IPv4 na interface interna**: marque a caixa de seleção se desejar aplicar um endereço IPv4 à interface interna do servidor de borda ou do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="8e622-149">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="8e622-150">**Habilitar o IPv6 na interface interna**: marque a caixa de seleção se desejar aplicar um endereço IPv6 à interface interna do servidor de borda ou do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="8e622-150">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="8e622-151">**Habilitar IPv4 na interface externa**: marque a caixa de seleção se desejar aplicar um endereço IPv4 à interface externa do servidor de borda ou do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="8e622-151">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="8e622-152">**Habilitar o IPv6 em uma interface externa**: marque a caixa de seleção se desejar aplicar um endereço IPv6 à interface externa do servidor de borda ou do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="8e622-152">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <span data-ttu-id="8e622-153">Você também pode configurar o servidor de borda ou o pool de bordas para usar um endereço de conversão de endereços de rede para os endereços IP externos.</span><span class="sxs-lookup"><span data-stu-id="8e622-153">You can also configure the Edge Server or Edge pool to use a network address translation address for the external IP addresses.</span></span> <span data-ttu-id="8e622-154">Para fazer isso, marque a caixa de seleção **o endereço IP externo deste pool de bordas é convertido pela NAT**.</span><span class="sxs-lookup"><span data-stu-id="8e622-154">You do this by selecting the check box **The external IP address of this Edge pool is translated by NAT**.</span></span>

8.  <span data-ttu-id="8e622-155">Em **FQDNs externos**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-155">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-156">Se, em **Selecione os recursos** , você optar por usar um único FQDN e um único endereço IP para o acesso SIP, serviço de Webconferência e a/V Edge, digite o FQDN externo no **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-156">If in **Select features** you chose to use a single FQDN and IP address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8e622-157">Se você escolher essa opção, especifique um número de porta diferente para cada um dos serviços de borda (configurações de porta recomendadas: 5061 para serviço de borda de acesso, 444 para serviço de borda de Webconferência e 443 para serviço de borda A/V).</span><span class="sxs-lookup"><span data-stu-id="8e622-157">If you choose this option, you must specify a different port number for each of the edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="8e622-158">Selecionar essa opção pode ajudar a evitar possíveis problemas de conectividade e simplificar a configuração porque você pode usar o mesmo número de porta (por exemplo, 443) para todos os três serviços.</span><span class="sxs-lookup"><span data-stu-id="8e622-158">Selecting this option can help prevent potential connectivity issues, and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="8e622-159">Se, **em Selecione os recursos** , você não tiver optado por usar um único FQDN e endereço IP, digite os FQDNs externos para **acesso SIP**, **conferência na Web** e **vídeo de áudio**, mantendo as portas padrão.</span><span class="sxs-lookup"><span data-stu-id="8e622-159">If in **Select features** you did not chose to use a single FQDN and IP Address, type the External FQDNs for **SIP Access**, **Web Conferencing** and **Audio Video**, keeping the default ports.</span></span>

9.  <span data-ttu-id="8e622-160">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="8e622-160">Click **Next**.</span></span>

10. <span data-ttu-id="8e622-161">Em **definir o endereço IP interno**, digite o endereço IP do seu servidor de borda em **endereço IPv4 interno** e **endereço IPv6 interno** como apropriado para seus requisitos.</span><span class="sxs-lookup"><span data-stu-id="8e622-161">In **Define the Internal IP address**, type the IP address of your Edge Server in **Internal IPv4 address** and **Internal IPv6 address** as is appropriate for your requirements.</span></span> <span data-ttu-id="8e622-162">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="8e622-162">Click **Next**.</span></span>

11. <span data-ttu-id="8e622-163">Em **definir o endereço IP externo**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-163">In **Define the External IP address**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-164">Se você optou por usar um único FQDN e um único endereço IP para o acesso SIP, serviço de Webconferência e A/V Edge, digite o endereço IPv4 externo do servidor de borda no **acesso SIP** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-164">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 address of the Edge Server in **SIP Access**, and then, click **Next**.</span></span>
    
      - <span data-ttu-id="8e622-165">Se você optou por usar endereços IPv6, digite o endereço IPv6 externo do servidor de borda em **acesso SIP** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-165">If you chose to use IPv6 addresses, type the external IPv6 address of the Edge Server in **SIP Access**, and then, click **Next**.</span></span>
    
      - <span data-ttu-id="8e622-166">Se você não optou por usar um único FQDN e um único endereço IP para o acesso SIP, serviço de Webconferência e a/V Edge, digite os endereços IPv4 externos do servidor de borda no **acesso SIP**, **conferência via Web** e **conferência a/v** e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-166">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 addresses of the Edge Server in **SIP Access**, **Web Conferencing**, and **A/V Conferencing**, and then click **Next**.</span></span>
    
      - <span data-ttu-id="8e622-167">Se você optou por usar endereços IPv6 e não optou por usar um único FQDN e um único endereço IP para o acesso SIP, serviço de Webconferência e a/V Edge, digite os endereços IPv6 externos do servidor de borda em **acesso SIP**, **conferência via Web** e **conferência a/v** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-167">If you chose to use IPv6 addresses and did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 addresses of the Edge Server in **SIP Access**, **Web Conferencing**, and **A/V Conferencing**, and then click **Next**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8e622-168">Se você não optou por habilitar e atribuir endereçamento IPv6, esta caixa de diálogo não será exibida.</span><span class="sxs-lookup"><span data-stu-id="8e622-168">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

        
        </div>

12. <span data-ttu-id="8e622-169">Se você optou por usar o NAT, será exibida uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8e622-169">If you chose to use NAT, a dialog box appears.</span></span> <span data-ttu-id="8e622-170">Em **endereço IPv4 público para o serviço de borda a/V**, digite o endereço IPv4 público a ser traduzido por Nat e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-170">In **Public IPv4 address for the A/V Edge service**, type the public IPv4 address to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e622-171">Este deve ser o endereço IP externo do serviço de borda A/V.</span><span class="sxs-lookup"><span data-stu-id="8e622-171">This should be the external IP address of the A/V Edge service.</span></span>

    
    </div>

13. <span data-ttu-id="8e622-172">Se você optou por usar o NAT e endereços IPv6, será exibida uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8e622-172">If you chose to use NAT and IPv6 addresses, a dialog box appears.</span></span> <span data-ttu-id="8e622-173">Em **endereço IPv6 público para o serviço de borda a/V**, digite o endereço IPv6 público a ser traduzido por Nat e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-173">In **Public IPv6 address for the A/V Edge service**, type the public IPv6 address to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e622-174">Este deve ser o endereço IP externo do serviço de borda A/V.</span><span class="sxs-lookup"><span data-stu-id="8e622-174">This should be the external IP address of the A/V Edge service.</span></span>

    
    </div>

14. <span data-ttu-id="8e622-175">Em **definir o próximo salto**, no **próximo pool de saltos**, selecione o nome do pool interno, que pode ser um pool de front-ends ou um pool padrão de edição.</span><span class="sxs-lookup"><span data-stu-id="8e622-175">In **Define the next hop**, in **Next hop pool**, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="8e622-176">Ou, se a sua implantação incluir um director, selecione o diretor.</span><span class="sxs-lookup"><span data-stu-id="8e622-176">Or, if your deployment includes a Director, select the Director.</span></span> <span data-ttu-id="8e622-177">Em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-177">Then, click **Next**.</span></span>

15. <span data-ttu-id="8e622-178">Em **pools de front-end**, especifique um ou mais pools internos, que podem incluir pools front-ends e servidores Standard Edition, a serem associados a esse servidor de borda, selecionando os nomes dos pools internos que devem usar esse servidor de borda para comunicação com usuários externos com suporte.</span><span class="sxs-lookup"><span data-stu-id="8e622-178">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pools that are to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e622-179">Somente um pool de bordas com carga balanceada ou um servidor de borda única pode ser associado a cada pool interno para o tráfego A/V.</span><span class="sxs-lookup"><span data-stu-id="8e622-179">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="8e622-180">Se você já tiver um pool interno associado a um pool de bordas ou servidor de borda, um aviso será exibido indicando que o pool interno já está associado a um pool de bordas ou um servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-180">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="8e622-181">Se você selecionar um pool que já esteja associado a outro servidor de borda, ele alterará a associação.</span><span class="sxs-lookup"><span data-stu-id="8e622-181">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

16. <span data-ttu-id="8e622-182">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="8e622-182">Click **Finish**.</span></span>

17. <span data-ttu-id="8e622-183">Publicar sua topologia.</span><span class="sxs-lookup"><span data-stu-id="8e622-183">Publish your topology.</span></span>

</div>

<div>

## <a name="to-define-the-topology-for-a-dns-load-balanced-edge-server-pool"></a><span data-ttu-id="8e622-184">Para definir a topologia de um pool de servidores de borda balanceada para carga de DNS</span><span class="sxs-lookup"><span data-stu-id="8e622-184">To define the topology for a DNS load balanced Edge Server pool</span></span>

1.  <span data-ttu-id="8e622-185">Iniciar o construtor de topologias: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Construtor de topologias do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="8e622-185">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="8e622-186">Na árvore de console, expanda o site no qual você deseja implantar servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-186">In the console tree, expand the site in which you want to deploy Edge Servers.</span></span>

3.  <span data-ttu-id="8e622-187">Clique com o botão direito do mouse em **conjuntos de bordas** e clique em **novo pool de bordas**.</span><span class="sxs-lookup"><span data-stu-id="8e622-187">Right-click **Edge Pools**, and then click **New Edge Pool**.</span></span>

4.  <span data-ttu-id="8e622-188">Em **definir o novo pool de bordas**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-188">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="8e622-189">Em **definir o FQDN do pool de bordas**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-189">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-190">Em **pool FQDN**, digite o nome de domínio totalmente qualificado (FQDN) para a conexão interna do pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-190">In **Pool FQDN**, type the fully qualified domain name (FQDN) for the internal connection of the Edge pool.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="8e622-191">O nome que você especificar para o pool deve ser o nome do pool de bordas internas.</span><span class="sxs-lookup"><span data-stu-id="8e622-191">The name you specify for the pool must be the internal edge pool name.</span></span> <span data-ttu-id="8e622-192">Isso deve ser definido como um FQDN.</span><span class="sxs-lookup"><span data-stu-id="8e622-192">This must be defined as a FQDN.</span></span> <span data-ttu-id="8e622-193">O Construtor de Topologias usa FQDNs, não nomes curtos.</span><span class="sxs-lookup"><span data-stu-id="8e622-193">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="8e622-194">Use apenas caracteres padrão (incluindo A–Z, a–z, 0–9 e hifens) ao atribuir FQDNs de seus Lync Servers, Servidores de Borda e pools.</span><span class="sxs-lookup"><span data-stu-id="8e622-194">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="8e622-195">Não use caracteres Unicode ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="8e622-195">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="8e622-196">Os caracteres não padrão em um FQDN geralmente não são compatíveis com o DNS externo e CAs públicas (quando o FQDN deve ser atribuído ao SN no certificado).</span><span class="sxs-lookup"><span data-stu-id="8e622-196">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span>

        
        </div>
    
      - <span data-ttu-id="8e622-197">Clique em **vários pools de computador** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-197">Click **Multiple computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="8e622-198">Em **selecionar recursos**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-198">In **Select features**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-199">Se você pretende usar um único FQDN e endereço IP para o acesso SIP, serviço de Webconferência do Lync Server 2013 e serviços de borda A/V, marque a caixa de seleção **usar um único FQDN e endereço IP** .</span><span class="sxs-lookup"><span data-stu-id="8e622-199">If you plan to use a single FQDN and IP address for the SIP access, Lync Server 2013 Web Conferencing service and A/V Edge services, select the **Use a single FQDN and IP Address** check box.</span></span>
    
      - <span data-ttu-id="8e622-200">Se você planeja habilitar a Federação, marque a caixa de seleção **habilitar Federação para este pool de bordas (porta 5061)** .</span><span class="sxs-lookup"><span data-stu-id="8e622-200">If you plan to enable federation, select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span> <span data-ttu-id="8e622-201">Clique em **Avançar**</span><span class="sxs-lookup"><span data-stu-id="8e622-201">Click **Next**</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8e622-202">Você pode selecionar essa opção, mas somente um pool de bordas ou um servidor de borda em sua organização pode ser publicado externamente para Federação.</span><span class="sxs-lookup"><span data-stu-id="8e622-202">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="8e622-203">Todo o acesso de usuários federados, incluindo usuários públicos de mensagens instantâneas (IM), passam pelo mesmo pool de bordas ou servidor de borda única.</span><span class="sxs-lookup"><span data-stu-id="8e622-203">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="8e622-204">Por exemplo, se sua implantação incluir um pool de Borda ou um único Servidor de Borda implantado em Nova York e outro implantado em Londres e você habilitar o suporte para federação no pool de Borda de Nova York ou único Servidor de Borda, o tráfego do sinal para usuários federados passará pelo pool de Borda ou único Servidor de Borda de Nova York.</span><span class="sxs-lookup"><span data-stu-id="8e622-204">For instance, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="8e622-205">Isso se aplica inclusive para comunicações com usuários de Londres, embora um usuário interno de Londres chamando um usuário federado de Londres use o pool de Londres ou Servidor de Borda para tráfego de A/V.</span><span class="sxs-lookup"><span data-stu-id="8e622-205">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="8e622-206">Se você planeja dar suporte ao protocolo de mensagens extensíveis e presença (XMPP) para a sua implantação, marque a caixa de seleção **habilitar Federação de XMPP (porta 5269)**</span><span class="sxs-lookup"><span data-stu-id="8e622-206">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="8e622-207">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="8e622-207">Click **Next**.</span></span>

8.  <span data-ttu-id="8e622-208">Em **selecionar opções de IP**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-208">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-209">**Habilitar IPv4 na interface interna**: marque a caixa de seleção se desejar aplicar um endereço IPv4 à interface interna do servidor de borda ou do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="8e622-209">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="8e622-210">**Habilitar o IPv6 na interface interna**: marque a caixa de seleção se desejar aplicar um endereço IPv6 à interface interna do servidor de borda ou do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="8e622-210">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="8e622-211">**Habilitar IPv4 na interface externa**: marque a caixa de seleção se desejar aplicar um endereço IPv4 à interface externa do servidor de borda ou do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="8e622-211">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="8e622-212">**Habilitar o IPv6 em uma interface externa**: marque a caixa de seleção se desejar aplicar um endereço IPv6 à interface externa do servidor de borda ou do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="8e622-212">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <span data-ttu-id="8e622-213">Você também pode configurar o servidor de borda ou o pool de bordas para usar um endereço de conversão de endereços de rede para os endereços IP externos.</span><span class="sxs-lookup"><span data-stu-id="8e622-213">You can also configure the Edge Server or Edge pool to use a network address translation address for the external IP addresses.</span></span> <span data-ttu-id="8e622-214">Para fazer isso, marque a caixa de seleção **o endereço IP externo deste pool de bordas é convertido pela NAT**.</span><span class="sxs-lookup"><span data-stu-id="8e622-214">You do this by selecting the check box **The external IP address of this Edge pool is translated by NAT**.</span></span>

9.  <span data-ttu-id="8e622-215">Em **FQDNs externos**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-215">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-216">Se, em **Selecione os recursos** , você optar por usar um único FQDN e um único endereço IP para o acesso SIP, serviço de Webconferência e a/V Edge, digite o FQDN externo no **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-216">If in **Select features** you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8e622-217">Se você escolher essa opção, especifique um número de porta diferente para cada um dos serviços de borda (configurações de porta recomendadas: 5061 para serviço de borda de acesso, 444 para serviço de borda de Webconferência e 443 para serviço de borda A/V).</span><span class="sxs-lookup"><span data-stu-id="8e622-217">If you choose this option, you must specify a different port number for each of the Edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="8e622-218">Ao selecionar essa opção, você pode ajudar a evitar possíveis problemas de conectividade e simplificar a configuração porque pode usar o mesmo número de porta (por exemplo, 443) para todos os três serviços.</span><span class="sxs-lookup"><span data-stu-id="8e622-218">By selecting this option, you can help prevent potential connectivity issues and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="8e622-219">Se, em **Selecione os recursos** , você não tiver optado por usar um único FQDN e endereço IP, digite o FQDN escolhido para seu lado público do pool de bordas no **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-219">If in **Select features** you did not chose to use a single FQDN and IP Address, type the FQDN that you have chosen for your public facing side of the edge pool for in **SIP Access**.</span></span> <span data-ttu-id="8e622-220">Em **Webconferência**, digite o FQDN escolhido para o seu lado público do lado do pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-220">In **Web Conferencing**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="8e622-221">Em **áudio/vídeo**, digite o FQDN escolhido para seu lado público do lado do pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-221">In **Audio/Video**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="8e622-222">Use as portas padrão.</span><span class="sxs-lookup"><span data-stu-id="8e622-222">Use the default ports.</span></span>

10. <span data-ttu-id="8e622-223">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="8e622-223">Click **Next**.</span></span>

11. <span data-ttu-id="8e622-224">Em **definir os computadores neste pool**, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-224">In **Define the computers in this pool**, click **Add**.</span></span>

12. <span data-ttu-id="8e622-225">Em **endereço IP e FQDN internos**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-225">In **Internal FQDN and IP address**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-226">Em **endereço IPv4 interno**, digite o endereço IPv4 e o **endereço IPv6 interno** como apropriado para seus requisitos para o primeiro servidor de borda que você deseja criar nesse pool.</span><span class="sxs-lookup"><span data-stu-id="8e622-226">In **Internal IPv4 address**, type the IPv4 address and **Internal IPv6 address** as is appropriate for your requirements for the first Edge Server that you want to create in this pool.</span></span>
    
      - <span data-ttu-id="8e622-227">Em **FQDN interno**, digite o FQDN do primeiro servidor de borda que você deseja criar nesse pool.</span><span class="sxs-lookup"><span data-stu-id="8e622-227">In **Internal FQDN**, type the FQDN of the first Edge Server that you want to create in this pool.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8e622-228">O nome que você especificar dever ser idêntico ao nome de computador configurado no servidor.</span><span class="sxs-lookup"><span data-stu-id="8e622-228">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="8e622-229">Por padrão, o nome de computador de um computador que não faz parte de um domínio é um nome curto, não um FQDN.</span><span class="sxs-lookup"><span data-stu-id="8e622-229">By default, the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="8e622-230">O Construtor de Topologias usa FQDNs, não nomes curtos.</span><span class="sxs-lookup"><span data-stu-id="8e622-230">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="8e622-231">Portanto, você deverá configurar um sufixo DNS no nome do computador a ser implantado no Servidor de Borda que não ingressou no domínio.</span><span class="sxs-lookup"><span data-stu-id="8e622-231">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="8e622-232">Use somente caracteres padrão (incluindo A – Z, A – z, 0 – 9 e hifens) ao atribuir FQDNs dos seus servidores, servidores de borda, pools e matrizes do Lync.</span><span class="sxs-lookup"><span data-stu-id="8e622-232">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, pools, and arrays.</span></span> <span data-ttu-id="8e622-233">Não use caracteres Unicode ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="8e622-233">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="8e622-234">Os caracteres não padrão em um FQDN geralmente não são compatíveis com o DNS externo e CAs públicas (quando o FQDN deve ser atribuído ao SN no certificado).</span><span class="sxs-lookup"><span data-stu-id="8e622-234">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="8e622-235">Para obter detalhes sobre como adicionar um sufixo DNS a um nome de computador, consulte <A href="lync-server-2013-configure-dns-for-edge-support.md">Configurar o DNS para suporte de borda no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="8e622-235">For details about adding a DNS suffix to a computer name, see <A href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</A>.</span></span>

        
        </div>

13. <span data-ttu-id="8e622-236">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="8e622-236">Click **Next**.</span></span>

14. <span data-ttu-id="8e622-237">Em **definir os endereços IP externos**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-237">In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-238">Se você optou por usar um único FQDN e um único endereço IP para o acesso SIP, serviço de Webconferência e a/V Edge, digite o endereço IP externo do servidor de borda no **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-238">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IP address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="8e622-239">Se você não optou por usar um único FQDN e um único endereço IP para o serviço de acesso SIP, Web de Webconferência e o/V referencing, digite o endereço IP que você escolheu para o seu lado público deste servidor de pool de borda para **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-239">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IP address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="8e622-240">Em **Webconferência**, digite o endereço IP que você escolheu para o seu lado público deste servidor de pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-240">In **Web Conferencing**, type the IP address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="8e622-241">Em **conferência A/V**, digite o endereço IP escolhido para o seu lado público do lado público deste servidor de pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-241">In **A/V Conferencing**, type the IP address you have chosen for your public facing side of this Edge pool server.</span></span>

15. <span data-ttu-id="8e622-242">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="8e622-242">Click **Next**.</span></span>

16. <span data-ttu-id="8e622-243">Se você optou por habilitar endereços IPv6, em **definir os endereços IP externos**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-243">If you chose to enable IPv6 addresses, In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-244">Se você optou por usar um único FQDN e um único endereço IP para o acesso SIP, serviço de Webconferência e a/V Edge, digite o endereço IPv6 externo do servidor de borda no **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-244">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="8e622-245">Se você não optou por usar um único FQDN e um único endereço IP para o serviço de acesso SIP, Web de Webconferência e o/V referencing, digite o endereço IPv6 que você escolheu para o seu lado público deste servidor de pool de borda para **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-245">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IPv6 address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="8e622-246">Em **Webconferência**, digite o endereço IPv6 que você escolheu para seu lado público do lado público deste servidor de pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-246">In **Web Conferencing**, type the IPv6 address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="8e622-247">Em **conferência A/V**, digite o endereço IPv6 que você escolheu para seu lado público do lado público deste servidor de pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-247">In **A/V Conferencing**, type the IPv6 address you have chosen for your public facing side of this Edge pool server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e622-248">Se você não optou por habilitar e atribuir endereçamento IPv6, esta caixa de diálogo não será exibida.</span><span class="sxs-lookup"><span data-stu-id="8e622-248">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

    
    </div>

17. <span data-ttu-id="8e622-249">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="8e622-249">Click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e622-250">Agora, você verá o primeiro servidor de borda que você criou no pool na caixa de diálogo <STRONG>definir os computadores neste pool</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="8e622-250">You will now see the first Edge Server you created in your pool in the <STRONG>Define the computers in this pool</STRONG> dialog box.</span></span>

    
    </div>

18. <span data-ttu-id="8e622-251">Em **definir os computadores nesse pool**, clique em **Adicionar** e, em seguida, repita as etapas 11 a 14 para o segundo servidor de borda que você deseja adicionar ao seu pool de bordas.</span><span class="sxs-lookup"><span data-stu-id="8e622-251">In **Define the computers in this pool**, click **Add**, and then repeat steps 11 through 14 for the second Edge Server that you want to add to you Edge pool.</span></span>

19. <span data-ttu-id="8e622-252">Após repetir as etapas 11 a 14, clique em **Avançar** em **definir os computadores nesse pool**.</span><span class="sxs-lookup"><span data-stu-id="8e622-252">After you repeat steps 11 through 14, click **Next** in **Define the computers in this pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e622-253">Nesse ponto, você pode ver os dois servidores de borda no pool.</span><span class="sxs-lookup"><span data-stu-id="8e622-253">At this point, you can see both of the Edge Servers in your pool.</span></span>

    
    </div>

20. <span data-ttu-id="8e622-254">Se você optou por usar o NAT, será exibida uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8e622-254">If you chose to use NAT, a dialog box appears.</span></span> <span data-ttu-id="8e622-255">Em **endereço IP público**, digite os endereços IPv4 e IPv6 públicos (conforme apropriado) a serem convertidos por Nat e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-255">In **Public IP address**, type the public IPv4 and IPv6 (as appropriate) addresses to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e622-256">Deve ser o endereço IP externo da borda A/V.</span><span class="sxs-lookup"><span data-stu-id="8e622-256">This should be the external IP Address of the A/V Edge.</span></span>

    
    </div>

21. <span data-ttu-id="8e622-257">Em **definir o próximo salto**, na lista **próximo pool de saltos** , selecione o nome do pool interno, que pode ser um pool de front-ends ou um pool padrão de edição.</span><span class="sxs-lookup"><span data-stu-id="8e622-257">In **Define the next hop**, in the **Next hop pool** list, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="8e622-258">Ou, se a sua implantação incluir um director, selecione o nome do diretor.</span><span class="sxs-lookup"><span data-stu-id="8e622-258">Or, if your deployment includes a Director, select the name of the Director.</span></span> <span data-ttu-id="8e622-259">Em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-259">Then, click **Next**.</span></span>

22. <span data-ttu-id="8e622-260">Em **pools de front-end**, especifique um ou mais pools internos, que podem incluir pools front-ends e servidores Standard Edition, a serem associados a esse servidor de borda, selecionando os nomes dos pools internos que serão usados neste servidor de borda para comunicação com usuários externos com suporte.</span><span class="sxs-lookup"><span data-stu-id="8e622-260">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pool(s) that is to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e622-261">Somente um pool de bordas com carga balanceada ou um servidor de borda única pode ser associado a cada pool interno para o tráfego A/V.</span><span class="sxs-lookup"><span data-stu-id="8e622-261">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="8e622-262">Se você já tiver um pool interno associado a um pool de bordas ou servidor de borda, um aviso será exibido indicando que o pool interno já está associado a um pool de bordas ou um servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-262">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="8e622-263">Se você selecionar um pool que já esteja associado a outro servidor de borda, ele alterará a associação.</span><span class="sxs-lookup"><span data-stu-id="8e622-263">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

23. <span data-ttu-id="8e622-264">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="8e622-264">Click **Finish**.</span></span>

24. <span data-ttu-id="8e622-265">Publicar sua topologia.</span><span class="sxs-lookup"><span data-stu-id="8e622-265">Publish your topology.</span></span>

</div>

<div>

## <a name="to-define-the-topology-for-a-hardware-load-balanced-edge-server-pool"></a><span data-ttu-id="8e622-266">Para definir a topologia de um pool de servidores de borda com carga balanceada de hardware</span><span class="sxs-lookup"><span data-stu-id="8e622-266">To define the topology for a hardware load balanced Edge Server pool</span></span>

1.  <span data-ttu-id="8e622-267">Iniciar o construtor de topologias: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Construtor de topologias do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="8e622-267">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="8e622-268">Na árvore de console, expanda o site no qual você deseja implantar servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-268">In the console tree, expand the site in which you want to deploy Edge Servers.</span></span>

3.  <span data-ttu-id="8e622-269">Clique com o botão direito do mouse em **conjuntos de bordas** e selecione **novo pool de bordas**.</span><span class="sxs-lookup"><span data-stu-id="8e622-269">Right-click **Edge Pools**, and then select **New Edge Pool**.</span></span>

4.  <span data-ttu-id="8e622-270">Em **definir o novo pool de bordas**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-270">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="8e622-271">Em **definir o FQDN do pool de bordas**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-271">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-272">Em **FQDN**, digite o nome de domínio totalmente qualificado (FQDN) escolhido para o lado interno do pool de bordas.</span><span class="sxs-lookup"><span data-stu-id="8e622-272">In **FQDN**, type the fully qualified domain name (FQDN) you have chosen for the internal side of the Edge pool.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="8e622-273">O nome que você especificar para o pool deve ser o nome do pool de bordas internas.</span><span class="sxs-lookup"><span data-stu-id="8e622-273">The name you specify for the pool must be the internal edge pool name.</span></span> <span data-ttu-id="8e622-274">Isso deve ser definido como um FQDN.</span><span class="sxs-lookup"><span data-stu-id="8e622-274">This must be defined as a FQDN.</span></span> <span data-ttu-id="8e622-275">O Construtor de Topologias usa FQDNs, não nomes curtos.</span><span class="sxs-lookup"><span data-stu-id="8e622-275">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="8e622-276">Use apenas caracteres padrão (incluindo A–Z, a–z, 0–9 e hifens) ao atribuir FQDNs de seus Lync Servers, Servidores de Borda e pools.</span><span class="sxs-lookup"><span data-stu-id="8e622-276">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="8e622-277">Não use caracteres Unicode ou sublinhados.</span><span class="sxs-lookup"><span data-stu-id="8e622-277">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="8e622-278">Os caracteres não padrão em um FQDN geralmente não são compatíveis com o DNS externo e CAs públicas (quando o FQDN deve ser atribuído ao SN no certificado).</span><span class="sxs-lookup"><span data-stu-id="8e622-278">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span>

        
        </div>
    
    <!-- end list -->
    
      - <span data-ttu-id="8e622-279">Clique em **vários pool de computador** e, em seguida, em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-279">Click **Multiple computer pool**, and then **Next**.</span></span>

6.  <span data-ttu-id="8e622-280">Em **selecionar recursos** , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-280">In **Select features** do the following:</span></span>
    
      - <span data-ttu-id="8e622-281">Se você pretende usar um único FQDN e endereço IP para o serviço de acesso SIP, serviço de Webconferência do Lync Server e A/V Edge, marque a caixa de seleção **usar um único fqdn & endereço IP** .</span><span class="sxs-lookup"><span data-stu-id="8e622-281">If you plan to use a single FQDN and IP address for the SIP access service, Lync Server Web Conferencing service, and A/V Edge service, select the **Use a single FQDN & IP Address** check box.</span></span>
    
      - <span data-ttu-id="8e622-282">Se você planeja habilitar a Federação, marque a caixa de seleção **habilitar Federação para este pool de bordas (porta 5061)** .</span><span class="sxs-lookup"><span data-stu-id="8e622-282">If you plan to enable federation, select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8e622-283">Você pode selecionar essa opção, mas somente um pool de bordas ou um servidor de borda em sua organização pode ser publicado externamente para Federação.</span><span class="sxs-lookup"><span data-stu-id="8e622-283">You can select this option, but only one Edge pool or Edge Server in your organization may be published externally for federation.</span></span> <span data-ttu-id="8e622-284">Todo o acesso de usuários federados, incluindo usuários públicos de mensagens instantâneas (IM), passam pelo mesmo pool de bordas ou servidor de borda única.</span><span class="sxs-lookup"><span data-stu-id="8e622-284">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="8e622-285">Por exemplo, se sua implantação incluir um pool de Borda ou um único Servidor de Borda implantado em Nova York e outro implantado em Londres e você habilitar o suporte para federação no pool de Borda de Nova York ou único Servidor de Borda, o tráfego do sinal para usuários federados passará pelo pool de Borda ou único Servidor de Borda de Nova York.</span><span class="sxs-lookup"><span data-stu-id="8e622-285">For instance, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="8e622-286">Isso se aplica inclusive para comunicações com usuários de Londres, embora um usuário interno de Londres chamando um usuário federado de Londres use o pool de Londres ou Servidor de Borda para tráfego de A/V.</span><span class="sxs-lookup"><span data-stu-id="8e622-286">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="8e622-287">Se você planeja dar suporte ao protocolo de mensagens extensíveis e presença (XMPP) para a sua implantação, marque a caixa de seleção **habilitar Federação de XMPP (porta 5269)**</span><span class="sxs-lookup"><span data-stu-id="8e622-287">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="8e622-288">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="8e622-288">Click **Next**.</span></span>

8.  <span data-ttu-id="8e622-289">Em **selecionar opções de IP**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-289">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-290">**Habilitar IPv4 na interface interna**: marque a caixa de seleção se desejar aplicar um endereço IPv4 à interface interna do servidor de borda ou do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="8e622-290">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="8e622-291">**Habilitar o IPv6 na interface interna**: marque a caixa de seleção se desejar aplicar um endereço IPv6 à interface interna do servidor de borda ou do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="8e622-291">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="8e622-292">**Habilitar IPv4 na interface externa**: marque a caixa de seleção se desejar aplicar um endereço IPv4 à interface externa do servidor de borda ou do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="8e622-292">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="8e622-293">**Habilitar o IPv6 em uma interface externa**: marque a caixa de seleção se desejar aplicar um endereço IPv6 à interface externa do servidor de borda ou do pool de bordas</span><span class="sxs-lookup"><span data-stu-id="8e622-293">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8e622-294"><STRONG>Não</STRONG> marque a caixa de seleção <STRONG>o endereço IP externo do pool de bordas é traduzido pela NAT</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="8e622-294"><STRONG>Do Not</STRONG> select the <STRONG>The external IP address of the Edge pool is translated by NAT</STRONG> check box.</span></span> <span data-ttu-id="8e622-295">Não há suporte para a conversão de endereços de rede (NAT) quando você está usando o balanceamento de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="8e622-295">Network address translation (NAT) is not supported when you are using hardware load balancing.</span></span>

    
    </div>

9.  <span data-ttu-id="8e622-296">Em **FQDNs externos**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-296">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-297">Se, em **Selecione os recursos** , você optar por usar um único FQDN e um único endereço IP para o acesso SIP, serviço de Webconferência e a/V Edge, digite o FQDN externo no **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-297">If in **Select features** you chose to use a single FQDN and IP address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8e622-298">Se optar por selecionar essa opção, você deve especificar um número de porta diferente para cada um dos serviços de borda (configurações de porta recomendadas: 5061 para serviço de borda de acesso, 444 para serviço de borda de Webconferência e 443 para serviço de borda A/V).</span><span class="sxs-lookup"><span data-stu-id="8e622-298">If you choose to select this option, you must specify a different port number for each of the Edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="8e622-299">Ao selecionar essa opção, você pode ajudar a evitar possíveis problemas de conectividade e simplificar a configuração porque pode usar o mesmo número de porta (por exemplo, 443) para todos os três serviços.</span><span class="sxs-lookup"><span data-stu-id="8e622-299">By selecting this option, you can help prevent potential connectivity issues and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="8e622-300">Se, em **Selecione os recursos** , você não tiver optado por usar um único FQDN e endereço IP, digite o FQDN escolhido para seu lado público do pool de bordas no **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-300">If in **Select features** you did not chose to use a single FQDN and IP address, type the FQDN that you have chosen for your public facing side of the edge pool for in **SIP Access**.</span></span> <span data-ttu-id="8e622-301">Em **Webconferência**, digite o FQDN escolhido para o seu lado público do lado do pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-301">In **Web Conferencing**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="8e622-302">Em **áudio/vídeo**, digite o FQDN escolhido para seu lado público do lado do pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-302">In **Audio/Video**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="8e622-303">Use as portas padrão.</span><span class="sxs-lookup"><span data-stu-id="8e622-303">Use the default ports.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="8e622-304">Estes serão os FQDNs VIP (IP virtual) de voltagem pública para o pool.</span><span class="sxs-lookup"><span data-stu-id="8e622-304">These will be the publicly facing virtual IP (VIP) FQDNs for the pool.</span></span>

        
        </div>

10. <span data-ttu-id="8e622-305">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="8e622-305">Click **Next**.</span></span>

11. <span data-ttu-id="8e622-306">Em **definir os computadores neste pool**, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-306">In **Define the computers in this pool**, click **Add**.</span></span>

12. <span data-ttu-id="8e622-307">Em **definir os endereços IP externos**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-307">In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-308">Se você optou por usar um único FQDN e um único endereço IP para o acesso SIP, serviço de Webconferência e a/V Edge, digite o endereço IPv4 externo do servidor de borda no **acesso SIP**. endereço IP externo do servidor de borda no **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-308">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 address of the Edge Server in **SIP Access**.external IP address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="8e622-309">Se você não optou por usar um único FQDN e um único endereço IP para o serviço de acesso SIP, Web de Webconferência e o/V referencing, digite o endereço IP que você escolheu para o seu lado público deste servidor de pool de borda para **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-309">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IP address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="8e622-310">Em **Webconferência**, digite o endereço IP que você escolheu para o seu lado público deste servidor de pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-310">In **Web Conferencing**, type the IP address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="8e622-311">Em **conferência A/V**, digite o endereço IP escolhido para o seu lado público do lado público deste servidor de pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-311">In **A/V Conferencing**, type the IP address you have chosen for your public facing side of this Edge pool server.</span></span>

13. <span data-ttu-id="8e622-312">Click **Next**.</span><span class="sxs-lookup"><span data-stu-id="8e622-312">Click **Next**.</span></span>

14. <span data-ttu-id="8e622-313">Se você optou por habilitar endereços IPv6, em **definir os endereços IP externos**, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8e622-313">If you chose to enable IPv6 addresses, In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="8e622-314">Se você optou por usar um único FQDN e um único endereço IP para o acesso SIP, serviço de Webconferência e a/V Edge, digite o endereço IPv6 externo do servidor de borda no **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-314">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="8e622-315">Se você não optou por usar um único FQDN e um único endereço IP para o serviço de acesso SIP, Web de Webconferência e o/V referencing, digite o endereço IPv6 que você escolheu para o seu lado público deste servidor de pool de borda para **acesso SIP**.</span><span class="sxs-lookup"><span data-stu-id="8e622-315">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IPv6 address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="8e622-316">Em **Webconferência**, digite o endereço IPv6 que você escolheu para seu lado público do lado público deste servidor de pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-316">In **Web Conferencing**, type the IPv6 address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="8e622-317">Em **conferência A/V**, digite o endereço IPv6 que você escolheu para seu lado público do lado público deste servidor de pool de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-317">In **A/V Conferencing**, type the IPv6 address you have chosen for your public facing side of this Edge pool server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e622-318">Se você não optou por habilitar e atribuir endereçamento IPv6, esta caixa de diálogo não será exibida.</span><span class="sxs-lookup"><span data-stu-id="8e622-318">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

    
    </div>

15. <span data-ttu-id="8e622-319">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="8e622-319">Click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e622-320">Agora, você verá o primeiro servidor de borda que você criou no pool na caixa de diálogo <STRONG>definir os computadores neste pool</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="8e622-320">You will now see the first Edge Server you created in your pool in the <STRONG>Define the computers in this pool</STRONG> dialog box.</span></span>

    
    </div>

16. <span data-ttu-id="8e622-321">Em **definir os computadores nesse pool**, clique em **Adicionar** e, em seguida, repita as etapas 11 a 14 para o segundo servidor de borda que você deseja adicionar ao seu pool de bordas.</span><span class="sxs-lookup"><span data-stu-id="8e622-321">In **Define the computers in this pool**, click **Add**, and then repeat steps 11 through 14 for the second Edge Server that you want to add to your Edge pool.</span></span>

17. <span data-ttu-id="8e622-322">Após repetir as etapas 11 a 14, clique em **Avançar** em **definir os computadores nesse pool**.</span><span class="sxs-lookup"><span data-stu-id="8e622-322">After you repeat steps 11 through 14, click **Next** in **Define the computers in this pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e622-323">Nesse ponto, você pode ver os dois servidores de borda no pool.</span><span class="sxs-lookup"><span data-stu-id="8e622-323">At this point, you can see both of the Edge Servers in your pool.</span></span>

    
    </div>

18. <span data-ttu-id="8e622-324">Em **definir o próximo salto**, na lista **próximo pool de saltos** , selecione o nome do pool interno, que pode ser um pool de front-ends ou um pool padrão de edição.</span><span class="sxs-lookup"><span data-stu-id="8e622-324">In **Define the next hop**, in the **Next hop pool** list, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="8e622-325">Ou, se a sua implantação incluir um director, selecione o nome do diretor.</span><span class="sxs-lookup"><span data-stu-id="8e622-325">Or, if your deployment includes a Director, select the name of the Director.</span></span> <span data-ttu-id="8e622-326">Em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="8e622-326">Then, click **Next**.</span></span>

19. <span data-ttu-id="8e622-327">Em **pools de front-end**, especifique um ou mais pools internos, que podem incluir pools front-ends e servidores Standard Edition, a serem associados a esse servidor de borda, selecionando os nomes dos pools internos que serão usados neste servidor de borda para comunicação com usuários externos com suporte.</span><span class="sxs-lookup"><span data-stu-id="8e622-327">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pool(s) that is to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8e622-328">Somente um pool de bordas com carga balanceada ou um servidor de borda única pode ser associado a cada pool interno para o tráfego A/V.</span><span class="sxs-lookup"><span data-stu-id="8e622-328">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="8e622-329">Se você já tiver um pool interno associado a um pool de bordas ou servidor de borda, um aviso será exibido indicando que o pool interno já está associado a um pool de bordas ou um servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="8e622-329">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="8e622-330">Se você selecionar um pool que já esteja associado a outro servidor de borda, ele alterará a associação.</span><span class="sxs-lookup"><span data-stu-id="8e622-330">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

20. <span data-ttu-id="8e622-331">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="8e622-331">Click **Finish**.</span></span>

21. <span data-ttu-id="8e622-332">Publicar sua topologia.</span><span class="sxs-lookup"><span data-stu-id="8e622-332">Publish your topology.</span></span>

<span data-ttu-id="8e622-333"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e622-333"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

