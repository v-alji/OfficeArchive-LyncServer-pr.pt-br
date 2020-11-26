---
title: Configurando federação SIP, federação XMPP e sistema de mensagens instântaneas público
description: Configuração de Federação SIP, Federação do XMPP e mensagens instantâneas públicas.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring SIP federation, XMPP federation and public instant messaging
ms:assetid: a6d04f0b-5cb8-4084-a3a2-d501938971f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205134(v=OCS.15)
ms:contentKeyID: 48184998
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7b83c29da75c99e7a338bfd7732aec8ec49cbf47
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432650"
---
# <a name="configuring-sip-federation-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="3741e-103">Configurando federação SIP, federação XMPP e sistema de mensagens instântaneas público no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3741e-103">Configuring SIP federation, XMPP federation and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3741e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3741e-104">

<span> </span></span></span>

<span data-ttu-id="3741e-105">_**Tópico da última modificação:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="3741e-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="3741e-106">Federação, conectividade de mensagens instantâneas públicas e protocolo de presença e mensagens extensíveis (XMPP) definem uma classe diferente de usuários externos – usuários federados.</span><span class="sxs-lookup"><span data-stu-id="3741e-106">Federation, public instant messaging connectivity and Extensible Messaging and Presence Protocol (XMPP) define a different class of external users – Federated users.</span></span> <span data-ttu-id="3741e-107">Os usuários de uma implantação do Lync Server federado ou implantação do XMPP têm acesso a um conjunto limitado de serviços e são autenticados pela implantação externa.</span><span class="sxs-lookup"><span data-stu-id="3741e-107">Users of a federated Lync Server deployment or XMPP deployment have access to a limited set of services and are authenticated by the external deployment.</span></span> <span data-ttu-id="3741e-108">Os usuários remotos são membros da implantação do Lync Server e têm acesso a todos os serviços oferecidos pela sua implantação.</span><span class="sxs-lookup"><span data-stu-id="3741e-108">Remote users are members of your Lync Server deployment and have access to all services offered by your deployment.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="3741e-109">Uma data de fim da vida útil de junho de 2014 para AOL e Yahoo!</span><span class="sxs-lookup"><span data-stu-id="3741e-109">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="3741e-110">foi anunciado.</span><span class="sxs-lookup"><span data-stu-id="3741e-110">has been announced.</span></span> <span data-ttu-id="3741e-111">Para obter detalhes, consulte <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">suporte para conectividade de mensagens instantâneas públicas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="3741e-111">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="3741e-112">A conectividade de mensagens instantâneas públicas é um tipo especial de Federação que permite que um cliente do Lync Server acesse parceiros de mensagens instantâneas públicas configurados usando o Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="3741e-112">Public instant messaging connectivity is a special type of federation that allows a Lync Server client to access configured public Instant Messaging partners using the Lync 2013.</span></span> <span data-ttu-id="3741e-113">Os atuais parceiros de conectividade de mensagens instantâneas públicas são:</span><span class="sxs-lookup"><span data-stu-id="3741e-113">The current public instant messaging connectivity partners are:</span></span>

  - <span></span>  
    <span data-ttu-id="3741e-114">America Online</span><span class="sxs-lookup"><span data-stu-id="3741e-114">America Online</span></span>

  - <span></span>  
    <span data-ttu-id="3741e-115">Windows Live</span><span class="sxs-lookup"><span data-stu-id="3741e-115">Windows Live</span></span>

  - <span></span>  
    <span data-ttu-id="3741e-116">Instant\!</span><span class="sxs-lookup"><span data-stu-id="3741e-116">Yahoo\!</span></span>

<span data-ttu-id="3741e-117">Uma configuração pública de conectividade de mensagens instantâneas permite que os usuários do Lync acessem usuários de conectividade de mensagens instantâneas públicas:</span><span class="sxs-lookup"><span data-stu-id="3741e-117">A public instant messaging connectivity configuration allows Lync users access to public instant messaging connectivity users by:</span></span>

  - <span data-ttu-id="3741e-118">Mensagens instantâneas e presença</span><span class="sxs-lookup"><span data-stu-id="3741e-118">IM and Presence</span></span>

  - <span data-ttu-id="3741e-119">Visibilidade de contatos públicos de conectividade de mensagens instantâneas no cliente do Lync</span><span class="sxs-lookup"><span data-stu-id="3741e-119">Visibility of public instant messaging connectivity contacts in Lync client</span></span>

  - <span data-ttu-id="3741e-120">Pessoa a quem você conversa mensagens instantâneas com contatos</span><span class="sxs-lookup"><span data-stu-id="3741e-120">Person to person IM conversations with contacts</span></span>

  - <span data-ttu-id="3741e-121">Chamadas de áudio e vídeo com usuários do Windows Live</span><span class="sxs-lookup"><span data-stu-id="3741e-121">Audio and video calls with Windows Live users</span></span>

<span data-ttu-id="3741e-122">A Federação do Lync Server define um contrato entre a implantação do Lync Server e outras implantações do Office Communications Server 2007 R2 ou Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3741e-122">Lync Server federation defines an agreement between your Lync Server deployment and other Office Communications Server 2007 R2 or Lync Server deployments.</span></span> <span data-ttu-id="3741e-123">Uma configuração federada do Lync Server permite que os usuários do Lync acessem usuários federados da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="3741e-123">A Lync Server federated configuration allows Lync users access to federated users by:</span></span>

  - <span data-ttu-id="3741e-124">Mensagens instantâneas e presença</span><span class="sxs-lookup"><span data-stu-id="3741e-124">IM and Presence</span></span>

  - <span data-ttu-id="3741e-125">Criação de contatos federados no cliente do Lync</span><span class="sxs-lookup"><span data-stu-id="3741e-125">Creation of federated contacts in the Lync client</span></span>

<span data-ttu-id="3741e-126">A Federação XMPP define uma implantação externa baseada no protocolo de mensagens extensíveis e presença.</span><span class="sxs-lookup"><span data-stu-id="3741e-126">XMPP federation defines an external deployment based on the eXtensible Messaging and Presence Protocol.</span></span> <span data-ttu-id="3741e-127">Uma configuração do XMPP permite que os usuários do Lync acessem usuários de domínio do XMPP permitidos da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="3741e-127">An XMPP configuration allows Lync users access to allowed XMPP domain users by:</span></span>

  - <span data-ttu-id="3741e-128">Mensagem instantânea e presença – pessoa para pessoa apenas</span><span class="sxs-lookup"><span data-stu-id="3741e-128">IM and Presence – person to person only</span></span>

  - <span data-ttu-id="3741e-129">Criação de contatos federados do XMPP no cliente do Lync</span><span class="sxs-lookup"><span data-stu-id="3741e-129">Creation of XMPP federated contacts in the Lync client</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="3741e-p106">O recurso XMPP do Lync Server 2013 é testado pela Microsoft e ela oferece suporte para federação de mensagens instantâneas com o Google Talk. Para quaisquer outros sistemas XMPP, entre em contato com o fornecedor do mesmo para verificar se eles suportam federação com o Lync Server 2013, e para quaisquer recomendações de implantação ou solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="3741e-p106">The XMPP capability of Lync Server 2013 is tested and supported by Microsoft for instant messaging federation with Google Talk. For any other XMPP systems contact the third-party vendor to verify that they support federation with Lync Server 2013, and for any deployment or troubleshooting recommendations.</span></span>



</div>

<div>

## <a name="edge-server-external-federation-public-instant-messaging-connectivity-and-xmpp-users-deployment-process"></a><span data-ttu-id="3741e-132">Federação externa do servidor de borda, conectividade de mensagens instantâneas públicas e processo de implantação de usuários do XMPP</span><span class="sxs-lookup"><span data-stu-id="3741e-132">Edge Server External Federation, Public Instant Messaging Connectivity and XMPP Users Deployment Process</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3741e-133">Fase</span><span class="sxs-lookup"><span data-stu-id="3741e-133">Phase</span></span></th>
<th><span data-ttu-id="3741e-134">Etapas</span><span class="sxs-lookup"><span data-stu-id="3741e-134">Steps</span></span></th>
<th><span data-ttu-id="3741e-135">Permissões</span><span class="sxs-lookup"><span data-stu-id="3741e-135">Permissions</span></span></th>
<th><span data-ttu-id="3741e-136">Documentação</span><span class="sxs-lookup"><span data-stu-id="3741e-136">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3741e-137">Determinar as opções para adicionar à implantação de borda existente</span><span class="sxs-lookup"><span data-stu-id="3741e-137">Determine the options to add to the existing Edge deployment</span></span></p></td>
<td><p><span data-ttu-id="3741e-138">Execute o construtor de topologias para editar as configurações do servidor de borda e crie e publique a topologia.</span><span class="sxs-lookup"><span data-stu-id="3741e-138">Run Topology Builder to edit Edge Server settings and create and publish the topology.</span></span> <span data-ttu-id="3741e-139">A topologia de borda existente replicará as alterações do repositório de gerenciamento central para o servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="3741e-139">Your existing Edge topology will replicate changes from the Central Management store to the Edge Server.</span></span></p></td>
<td><p><span data-ttu-id="3741e-140">Grupo Administradores de domínio e grupo RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="3741e-140">Domain Admins group and RTCUniversalServerAdmins group</span></span></p>



> [!NOTE]
> <span data-ttu-id="3741e-141">Você pode editar uma topologia usando uma conta que seja membro do grupo usuários local, mas publicar uma topologia requer uma conta que seja membro do grupo Administradores do domínio e do grupo RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="3741e-141">You can edit a topology using an account that is a member of the local users group, but publishing a topology requires an account that is a member of the Domain Admins group and the RTCUniversalServerAdmins group</span></span>

</td>
<td><p><span data-ttu-id="3741e-142"><a href="lync-server-2013-building-an-edge-and-director-topology.md">Criando uma topologia de borda e de diretor no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3741e-142"><a href="lync-server-2013-building-an-edge-and-director-topology.md">Building an edge and Director topology in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3741e-143">Preparar-se para a instalação</span><span class="sxs-lookup"><span data-stu-id="3741e-143">Prepare for setup</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="3741e-144">Certifique-se de que os pré-requisitos do sistema sejam atendidos.</span><span class="sxs-lookup"><span data-stu-id="3741e-144">Ensure that system prerequisites are met.</span></span></p></li>
<li><p><span data-ttu-id="3741e-145">Configurar registros DNS internos e externos para dar suporte à conectividade de mensagens instantâneas, ao agrupamento do Lync e à Federação do XMPP</span><span class="sxs-lookup"><span data-stu-id="3741e-145">Configure internal and external DNS records, to support public instant messaging connectivity, Lync Federation and XMPP Federation</span></span></p></li>
<li><p><span data-ttu-id="3741e-146">Configurar portas e protocolos no firewall para dar suporte aos tipos de Federação que você está implantando</span><span class="sxs-lookup"><span data-stu-id="3741e-146">Configure ports and protocols at the firewall to support the types of federation that you are deploying</span></span></p></li>
<li><p><span data-ttu-id="3741e-147">Obter e instalar certificados públicos.</span><span class="sxs-lookup"><span data-stu-id="3741e-147">Obtain and install public certificates.</span></span> <span data-ttu-id="3741e-148">O tempo necessário para obter certificados depende de qual a autoridade de certificação (CA) emite o certificado.</span><span class="sxs-lookup"><span data-stu-id="3741e-148">The time required to obtain certificates depends on which certification authority (CA) issues the certificate.</span></span> <span data-ttu-id="3741e-149">Esta etapa é opcional neste ponto da implantação.</span><span class="sxs-lookup"><span data-stu-id="3741e-149">This step is optional at this point in the deployment.</span></span> <span data-ttu-id="3741e-150">Se você não executar esta etapa neste ponto, deverá fazê-lo durante a configuração do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="3741e-150">If you do not perform this step at this point, you must do it during Edge Server configuration.</span></span> <span data-ttu-id="3741e-151">O serviço do servidor de borda não pode ser iniciado até que os certificados sejam obtidos</span><span class="sxs-lookup"><span data-stu-id="3741e-151">The Edge Server service cannot be started until certificates are obtained</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="3741e-152">Conforme apropriado para a sua organização, como essas funções geralmente são divididas entre vários grupos de trabalho</span><span class="sxs-lookup"><span data-stu-id="3741e-152">As appropriate to your organization, as these roles are typically split amongst numerous work groups</span></span></p></td>
<td><p><span data-ttu-id="3741e-153"><a href="lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md">Planejando o SIP, a Federação do XMPP e o sistema de mensagens instantâneas públicas no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3741e-153"><a href="lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3741e-154">Configurar servidores de borda para cenários de Federação</span><span class="sxs-lookup"><span data-stu-id="3741e-154">Set up Edge Servers for Federation Scenarios</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="3741e-155">Transportar o arquivo de configuração de topologia exportado para cada servidor de borda ou permitir que a replicação seja concluída</span><span class="sxs-lookup"><span data-stu-id="3741e-155">Transport the exported topology configuration file to each Edge Server or allow replication to complete</span></span></p></li>
<li><p><span data-ttu-id="3741e-156">Re-Run o assistente de implantação para instalar componentes de suporte para Federação</span><span class="sxs-lookup"><span data-stu-id="3741e-156">Re-Run the Deployment Wizard to install supporting components for Federation</span></span></p></li>
<li><p><span data-ttu-id="3741e-157">Configurar os servidores de borda</span><span class="sxs-lookup"><span data-stu-id="3741e-157">Configure the Edge Servers</span></span></p></li>
<li><p><span data-ttu-id="3741e-158">Solicitar e instalar certificados para cada servidor de borda</span><span class="sxs-lookup"><span data-stu-id="3741e-158">Request and install certificates for each Edge Server</span></span></p></li>
<li><p><span data-ttu-id="3741e-159">Reiniciar os serviços do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="3741e-159">Restart the Edge Server services</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="3741e-160">Grupo Administradores</span><span class="sxs-lookup"><span data-stu-id="3741e-160">Administrators group</span></span></p></td>
<td><p><span data-ttu-id="3741e-161"><a href="lync-server-2013-setting-up-lync-federation.md">Configuração de federação do Lync no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3741e-161"><a href="lync-server-2013-setting-up-lync-federation.md">Setting up Lync federation in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="3741e-162"><a href="lync-server-2013-setting-up-public-instant-messaging-connectivity.md">Configurar conectividade de mensagens instantâneas públicas no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3741e-162"><a href="lync-server-2013-setting-up-public-instant-messaging-connectivity.md">Setting up public instant messaging connectivity in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="3741e-163"><a href="lync-server-2013-setting-up-xmpp-federation.md">Configurando federação de XMPP no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3741e-163"><a href="lync-server-2013-setting-up-xmpp-federation.md">Setting up XMPP federation in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3741e-164">Configurar o suporte para acesso de usuário externo.</span><span class="sxs-lookup"><span data-stu-id="3741e-164">Configure support for external user access.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="3741e-165">Usar o painel de controle do Lync Server acesso externo do usuário</span><span class="sxs-lookup"><span data-stu-id="3741e-165">Use the Lync Server Control Panel External User Access</span></span></p></li>
<li><p><span data-ttu-id="3741e-166">Configurar a política de acesso externo para permitir comunicações com usuários federados ou usuários públicos</span><span class="sxs-lookup"><span data-stu-id="3741e-166">Configure External Access Policy to enable Communications with federated users or public users</span></span></p></li>
<li><p><span data-ttu-id="3741e-167">Configurar domínios federados SIP para permitir ou bloquear domínios</span><span class="sxs-lookup"><span data-stu-id="3741e-167">Configure SIP Federated Domains to Allow or Block domains</span></span></p></li>
<li><p><span data-ttu-id="3741e-168">Habilitar provedores federados SIP para provedores de conectividade de mensagens instantâneas públicas</span><span class="sxs-lookup"><span data-stu-id="3741e-168">Enable SIP Federated Providers for public instant messaging connectivity providers</span></span></p></li>
<li><p><span data-ttu-id="3741e-169">Configurar parceiros federados do XMPP por domínio XMPP</span><span class="sxs-lookup"><span data-stu-id="3741e-169">Configure XMPP Federated Partners per XMPP domain</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="3741e-170">Grupo RTCUniversalServerAdmins ou conta de usuário atribuída à função CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="3741e-170">RTCUniversalServerAdmins group or user account that is assigned to the CSAdministrator role</span></span></p></td>
<td><p><span data-ttu-id="3741e-171"><a href="lync-server-2013-configuring-support-for-external-user-access.md">Configurando suporte para acesso de usuário externo no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3741e-171"><a href="lync-server-2013-configuring-support-for-external-user-access.md">Configuring support for external user access in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="3741e-172"><a href="lync-server-2013-configure-media-encryption-for-public-providers.md">Configurar criptografia de mídia para fornecedores públicos no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3741e-172"><a href="lync-server-2013-configure-media-encryption-for-public-providers.md">Configure media encryption for public providers in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3741e-173">Verificar a configuração do servidor de borda</span><span class="sxs-lookup"><span data-stu-id="3741e-173">Verify your Edge Server configuration</span></span></p></td>
<td><p><span data-ttu-id="3741e-174">Verificar a conectividade do servidor e a replicação de dados de configuração de servidores internos</span><span class="sxs-lookup"><span data-stu-id="3741e-174">Verify server connectivity and replication of configuration data from internal servers</span></span></p></td>
<td><p><span data-ttu-id="3741e-175">Para a verificação da replicação, do grupo RTCUniversalServerAdmins ou da conta de usuário que é atribuída ao CSAdministrator de verificação de roleFor da conectividade do usuário, um usuário para cada tipo de usuário federado</span><span class="sxs-lookup"><span data-stu-id="3741e-175">For verification of replication, RTCUniversalServerAdmins group or user account that is assigned to the CSAdministrator roleFor verification of user connectivity, a user for each type of Federated user</span></span></p></td>
<td><p><span data-ttu-id="3741e-176"><a href="lync-server-2013-verifying-your-edge-deployment.md">Verificando a implantação de borda no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="3741e-176"><a href="lync-server-2013-verifying-your-edge-deployment.md">Verifying your edge deployment in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="3741e-177"><a href="lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md">Exemplo de configuração de XMPP no Lync Server 2013 – federação XMPP com Google Talk</a></span><span class="sxs-lookup"><span data-stu-id="3741e-177"><a href="lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</a></span></span></p></td>
</tr><span data-ttu-id="3741e-178">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3741e-178">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

