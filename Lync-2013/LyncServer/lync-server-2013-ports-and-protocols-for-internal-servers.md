---
title: 'Lync Server 2013: portas e protocolos para servidores internos'
description: 'Lync Server 2013: portas e protocolos para servidores internos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Ports and protocols for internal servers
ms:assetid: c94063f1-e802-4a61-be90-022fc185335e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398833(v=OCS.15)
ms:contentKeyID: 48185402
ms.date: 04/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7d8f12c78c5dec5caacaeb1156f4d228b7cd591
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424244"
---
# <a name="ports-and-protocols-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="808b1-103">Portas e protocolos para servidores internos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="808b1-103">Ports and protocols for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="808b1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="808b1-104">

<span> </span></span></span>

<span data-ttu-id="808b1-105">_**Tópico da última modificação:** 2016-04-06_</span><span class="sxs-lookup"><span data-stu-id="808b1-105">_**Topic Last Modified:** 2016-04-06_</span></span>

<span data-ttu-id="808b1-106">Esta seção resume as portas e os protocolos usados por servidores, balanceadores de carga e clientes em uma implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="808b1-106">This section summarizes the ports and protocols used by servers, load balancers, and clients in a Lync Server deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="808b1-107">Os clientes do Lync e do Communicator, quando envolvidos em uma comunicação de um para um, geralmente são chamados de ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="808b1-107">Lync and Communicator clients when involved in a one to one communication, is often referred to as peer-to-peer.</span></span> <span data-ttu-id="808b1-108">Tecnicamente, os dois clientes estão se comunicando em uma conversa de uma ou uma, com a IMMCU (unidade de controle Multipoint) do chat no meio.</span><span class="sxs-lookup"><span data-stu-id="808b1-108">Technically, the two clients are communicating in a one to one conversation, with the Instant Messaging multipoint control unit (IMMCU) in the middle.</span></span> <span data-ttu-id="808b1-109">O IMMCU é um componente do servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="808b1-109">The IMMCU is a component of Front End Server.</span></span> <span data-ttu-id="808b1-110">Colocar o IMMCU no fluxo de trabalho de comunicação necessário permite a gravação de detalhes da chamada e outros recursos que o servidor de front-end permite.</span><span class="sxs-lookup"><span data-stu-id="808b1-110">Placing the IMMCU in the required communication workflow allows call detail recording and other features that the Front End Server enables.</span></span> <span data-ttu-id="808b1-111">A comunicação é de uma porta de origem dinâmica no cliente para a porta de servidor front-end TLS/TCP/5061 (pressupondo o uso da segurança da camada de transporte recomendada).</span><span class="sxs-lookup"><span data-stu-id="808b1-111">Communication is from a dynamic source port on the client to the Front End Server port TLS/TCP/5061 (assuming the use of the recommended transport layer security).</span></span> <span data-ttu-id="808b1-112">Por design, a comunicação ponto a ponto (bem como mensagens instantâneas de vários participantes) só é possível quando o Lync Server e o IMMCU estão ativos e disponíveis.</span><span class="sxs-lookup"><span data-stu-id="808b1-112">By design, peer-to-peer communication (as well as multi-party IM) is possible only when Lync Server and the IMMCU is active and available.</span></span>



</div>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="808b1-113">Detalhes de protocolo e porta</span><span class="sxs-lookup"><span data-stu-id="808b1-113">Port and Protocol Details</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="808b1-114">O Firewall do Windows deve estar em execução antes de iniciar os serviços do Lync Server em um servidor, pois isso ocorre quando o Lync Server abre as portas obrigatórias no firewall.</span><span class="sxs-lookup"><span data-stu-id="808b1-114">Windows Firewall must be running before you start the Lync Server services on a server, because that is when Lync Server opens the required ports in the firewall.</span></span>



</div>

<span data-ttu-id="808b1-115">Para obter detalhes sobre a configuração de firewall para componentes de borda, consulte [determinar requisitos de firewall e porta externo A/V para o Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="808b1-115">For details about firewall configuration for edge components, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

<span data-ttu-id="808b1-116">A tabela a seguir lista as portas que precisam ser abertas em cada função de servidor interno.</span><span class="sxs-lookup"><span data-stu-id="808b1-116">The following table lists the ports that need to be open on each internal server role.</span></span>

### <a name="required-server-ports-by-server-role"></a><span data-ttu-id="808b1-117">Portas do servidor necessárias (por Função de servidor)</span><span class="sxs-lookup"><span data-stu-id="808b1-117">Required Server Ports (by Server Role)</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="808b1-118">Função de servidor</span><span class="sxs-lookup"><span data-stu-id="808b1-118">Server role</span></span></th>
<th><span data-ttu-id="808b1-119">Nome do serviço</span><span class="sxs-lookup"><span data-stu-id="808b1-119">Service name</span></span></th>
<th><span data-ttu-id="808b1-120">Porta</span><span class="sxs-lookup"><span data-stu-id="808b1-120">Port</span></span></th>
<th><span data-ttu-id="808b1-121">Protocolo</span><span class="sxs-lookup"><span data-stu-id="808b1-121">Protocol</span></span></th>
<th><span data-ttu-id="808b1-122">Notas</span><span class="sxs-lookup"><span data-stu-id="808b1-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="808b1-123">Todos os servidores</span><span class="sxs-lookup"><span data-stu-id="808b1-123">All Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-124">Navegador do SQL</span><span class="sxs-lookup"><span data-stu-id="808b1-124">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="808b1-125">1434</span><span class="sxs-lookup"><span data-stu-id="808b1-125">1434</span></span></p></td>
<td><p><span data-ttu-id="808b1-126">UDP</span><span class="sxs-lookup"><span data-stu-id="808b1-126">UDP</span></span></p></td>
<td><p><span data-ttu-id="808b1-127">Navegador do SQL para a cópia replicada local do banco de dados do repositório de gerenciamento central.</span><span class="sxs-lookup"><span data-stu-id="808b1-127">SQL Browser for the local replicated copy of the Central Management Store database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-128">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-128">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-129">Serviço Front-End do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-129">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="808b1-130">5060</span><span class="sxs-lookup"><span data-stu-id="808b1-130">5060</span></span></p></td>
<td><p><span data-ttu-id="808b1-131">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-131">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-132">Usada como opção pelos servidores Standard Edition e Servidores Front-End para rotas estáticas para serviços confiáveis, como servidores de controle de chamada remota.</span><span class="sxs-lookup"><span data-stu-id="808b1-132">Optionally used by Standard Edition servers and Front End Servers for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-133">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-133">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-134">Serviço Front-End do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-134">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="808b1-135">5061</span><span class="sxs-lookup"><span data-stu-id="808b1-135">5061</span></span></p></td>
<td><p><span data-ttu-id="808b1-136">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-136">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-137">Usada pelos servidores Standard Edition e pools de front-ends em todas as comunicações SIP internas entre servidores (MTLS), em comunicações SIP entre o servidor e o cliente (TLS) e em comunicações SIP entre os servidores front-end e os servidores de mediação (MTLS).</span><span class="sxs-lookup"><span data-stu-id="808b1-137">Used by Standard Edition servers and Front End pools for all internal SIP communications between servers (MTLS), for SIP communications between Server and Client (TLS) and for SIP communications between Front End Servers and Mediation Servers (MTLS).</span></span> <span data-ttu-id="808b1-138">Também usado para comunicações com o Monitoring Server.</span><span class="sxs-lookup"><span data-stu-id="808b1-138">Also used for communications with Monitoring Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-139">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-139">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-140">Serviço Front-End do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-140">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="808b1-141">444</span><span class="sxs-lookup"><span data-stu-id="808b1-141">444</span></span></p></td>
<td><p><span data-ttu-id="808b1-142">HTTPS</span><span class="sxs-lookup"><span data-stu-id="808b1-142">HTTPS</span></span></p>
<p><span data-ttu-id="808b1-143">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-143">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-144">Usado para comunicação HTTPS entre o foco (o componente do Lync Server que gerencia o estado da conferência) e os servidores individuais.</span><span class="sxs-lookup"><span data-stu-id="808b1-144">Used for HTTPS communication between the Focus (the Lync Server component that manages conference state) and the individual servers.</span></span></p>
<p><span data-ttu-id="808b1-145">Essa porta também é usada para comunicação TCP entre aparelhos de ramificação sobreviventes e servidores front-end.</span><span class="sxs-lookup"><span data-stu-id="808b1-145">This port is also used for TCP communication between Survivable Branch Appliances and Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-146">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-146">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-147">Serviço Front-End do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-147">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="808b1-148">135</span><span class="sxs-lookup"><span data-stu-id="808b1-148">135</span></span></p></td>
<td><p><span data-ttu-id="808b1-149">DCOM e RPC (controle de procedimento remoto)</span><span class="sxs-lookup"><span data-stu-id="808b1-149">DCOM and remote procedure call (RPC)</span></span></p></td>
<td><p><span data-ttu-id="808b1-150">Usada para operações com base em DCOM, como Movendo Usuários, Sincronização do Replicador do Usuário e Sincronização do Catálogo de Endereços.</span><span class="sxs-lookup"><span data-stu-id="808b1-150">Used for DCOM based operations such as Moving Users, User Replicator Synchronization, and Address Book Synchronization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-151">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-151">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-152">Serviço de conferência IM do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-152">Lync Server IM Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="808b1-153">5062</span><span class="sxs-lookup"><span data-stu-id="808b1-153">5062</span></span></p></td>
<td><p><span data-ttu-id="808b1-154">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-154">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-155">Usado para solicitações SIP de entrada para conferência de IM (mensagem instantânea).</span><span class="sxs-lookup"><span data-stu-id="808b1-155">Used for incoming SIP requests for instant messaging (IM) conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-156">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-156">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-157">Serviço de conferência Web do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-157">Lync Server Web Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="808b1-158">8057</span><span class="sxs-lookup"><span data-stu-id="808b1-158">8057</span></span></p></td>
<td><p><span data-ttu-id="808b1-159">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-159">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-160">Usada para escutar conexões PSOM (Modelo de Objeto Compartilhado Persistente) do cliente.</span><span class="sxs-lookup"><span data-stu-id="808b1-160">Used to listen for Persistent Shared Object Model (PSOM) connections from client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-161">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-161">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-162">Serviço de compatibilidade do Lync Server Web referencing</span><span class="sxs-lookup"><span data-stu-id="808b1-162">Lync Server Web Conferencing Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="808b1-163">8058</span><span class="sxs-lookup"><span data-stu-id="808b1-163">8058</span></span></p></td>
<td><p><span data-ttu-id="808b1-164">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-164">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-165">Usado para escutar conexões do modelo de objeto compartilhado persistente (PSOM) do cliente de reunião ao vivo e versões anteriores do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="808b1-165">Used to listen for Persistent Shared Object Model (PSOM) connections from the Live Meeting client and previous versions of Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-166">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-166">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-167">Serviço de conferência de áudio/vídeo do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-167">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="808b1-168">5063</span><span class="sxs-lookup"><span data-stu-id="808b1-168">5063</span></span></p></td>
<td><p><span data-ttu-id="808b1-169">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-169">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-170">Usada para solicitações SIP de entrada para conferência de áudio/vídeo (A/V).</span><span class="sxs-lookup"><span data-stu-id="808b1-170">Used for incoming SIP requests for audio/video (A/V) conferencing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-171">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-171">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-172">Serviço de conferência de áudio/vídeo do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-172">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="808b1-173">57501-65535</span><span class="sxs-lookup"><span data-stu-id="808b1-173">57501-65535</span></span></p></td>
<td><p><span data-ttu-id="808b1-174">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="808b1-174">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="808b1-175">Intervalo de porta de mídia usado para videoconferência.</span><span class="sxs-lookup"><span data-stu-id="808b1-175">Media port range used for video conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-176">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-176">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-177">Serviço de compatibilidade da Web do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-177">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="808b1-178">80</span><span class="sxs-lookup"><span data-stu-id="808b1-178">80</span></span></p></td>
<td><p><span data-ttu-id="808b1-179">HTTP</span><span class="sxs-lookup"><span data-stu-id="808b1-179">HTTP</span></span></p></td>
<td><p><span data-ttu-id="808b1-180">Usada para comunicação dos Servidores Front-End com os FQDNs do farm da web (as URLs usadas pelos componentes da web IIS) quando HTTPS não é usado.</span><span class="sxs-lookup"><span data-stu-id="808b1-180">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components) when HTTPS is not used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-181">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-181">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-182">Serviço de compatibilidade da Web do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-182">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="808b1-183">443</span><span class="sxs-lookup"><span data-stu-id="808b1-183">443</span></span></p></td>
<td><p><span data-ttu-id="808b1-184">HTTPS</span><span class="sxs-lookup"><span data-stu-id="808b1-184">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="808b1-185">Usado para comunicação dos servidores front-End no farm da web FQDNs (as URLs usadas pelos componentes da web do IIS).</span><span class="sxs-lookup"><span data-stu-id="808b1-185">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-186">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-186">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-187">Serviço de compatibilidade da Web do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-187">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="808b1-188">8080</span><span class="sxs-lookup"><span data-stu-id="808b1-188">8080</span></span></p></td>
<td><p><span data-ttu-id="808b1-189">TCP e HTTP</span><span class="sxs-lookup"><span data-stu-id="808b1-189">TCP and HTTP</span></span></p></td>
<td><p><span data-ttu-id="808b1-190">Usado pelos componentes da Web para acesso externo.</span><span class="sxs-lookup"><span data-stu-id="808b1-190">Used by web components for external access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-191">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-191">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-192">Servidor de componentes da Web</span><span class="sxs-lookup"><span data-stu-id="808b1-192">Web server component</span></span></p></td>
<td><p><span data-ttu-id="808b1-193">4443</span><span class="sxs-lookup"><span data-stu-id="808b1-193">4443</span></span></p></td>
<td><p><span data-ttu-id="808b1-194">HTTPS</span><span class="sxs-lookup"><span data-stu-id="808b1-194">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="808b1-195">Comunicações entre pools de front-end HTTPS (de Proxy Reverso) e HTTPS para conexão de Descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="808b1-195">HTTPS (from Reverse Proxy) and HTTPS Front End inter-pool communications for Autodiscover sign-in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-196">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-196">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-197">Servidor de componentes da Web</span><span class="sxs-lookup"><span data-stu-id="808b1-197">Web server component</span></span></p></td>
<td><p><span data-ttu-id="808b1-198">8060</span><span class="sxs-lookup"><span data-stu-id="808b1-198">8060</span></span></p></td>
<td><p><span data-ttu-id="808b1-199">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-199">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-200">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-200">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-201">Servidor de componentes da Web</span><span class="sxs-lookup"><span data-stu-id="808b1-201">Web server component</span></span></p></td>
<td><p><span data-ttu-id="808b1-202">8061</span><span class="sxs-lookup"><span data-stu-id="808b1-202">8061</span></span></p></td>
<td><p><span data-ttu-id="808b1-203">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-203">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-204">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-204">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-205">Componente dos serviços de mobilidade</span><span class="sxs-lookup"><span data-stu-id="808b1-205">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="808b1-206">5086</span><span class="sxs-lookup"><span data-stu-id="808b1-206">5086</span></span></p></td>
<td><p><span data-ttu-id="808b1-207">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-207">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-208">Porta SIP usada pelos processos internos dos Serviços de Mobilidade</span><span class="sxs-lookup"><span data-stu-id="808b1-208">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-209">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-209">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-210">Componente dos serviços de mobilidade</span><span class="sxs-lookup"><span data-stu-id="808b1-210">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="808b1-211">5087</span><span class="sxs-lookup"><span data-stu-id="808b1-211">5087</span></span></p></td>
<td><p><span data-ttu-id="808b1-212">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-212">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-213">Porta SIP usada pelos processos internos dos Serviços de Mobilidade</span><span class="sxs-lookup"><span data-stu-id="808b1-213">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-214">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-214">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-215">Componente dos serviços de mobilidade</span><span class="sxs-lookup"><span data-stu-id="808b1-215">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="808b1-216">443</span><span class="sxs-lookup"><span data-stu-id="808b1-216">443</span></span></p></td>
<td><p><span data-ttu-id="808b1-217">HTTPS</span><span class="sxs-lookup"><span data-stu-id="808b1-217">HTTPS</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-218">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-218">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-219">Serviço de atendedor do Lync Server Conferencing (conferência discada)</span><span class="sxs-lookup"><span data-stu-id="808b1-219">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="808b1-220">5064</span><span class="sxs-lookup"><span data-stu-id="808b1-220">5064</span></span></p></td>
<td><p><span data-ttu-id="808b1-221">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-221">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-222">Usada para solicitações SIP de entrada para conferência discada.</span><span class="sxs-lookup"><span data-stu-id="808b1-222">Used for incoming SIP requests for dial-in conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-223">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-223">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-224">Serviço de atendedor do Lync Server Conferencing (conferência discada)</span><span class="sxs-lookup"><span data-stu-id="808b1-224">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="808b1-225">5072</span><span class="sxs-lookup"><span data-stu-id="808b1-225">5072</span></span></p></td>
<td><p><span data-ttu-id="808b1-226">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-226">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-227">Usado para solicitações SIP de entrada do atendente (discagem por conferência).</span><span class="sxs-lookup"><span data-stu-id="808b1-227">Used for incoming SIP requests for Attendant (dial in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-228">Servidores Front-End que também executam um Servidor de Mediação Colocado</span><span class="sxs-lookup"><span data-stu-id="808b1-228">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="808b1-229">Serviço de mediação do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-229">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="808b1-230">5070</span><span class="sxs-lookup"><span data-stu-id="808b1-230">5070</span></span></p></td>
<td><p><span data-ttu-id="808b1-231">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-231">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-232">Usada pelo Servidor de Mediação para solicitações de entrada do Servidor Front-End para o Servidor de Mediação.</span><span class="sxs-lookup"><span data-stu-id="808b1-232">Used by the Mediation Server for incoming requests from the Front End Server to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-233">Servidores Front-End que também executam um Servidor de Mediação Colocado</span><span class="sxs-lookup"><span data-stu-id="808b1-233">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="808b1-234">Serviço de mediação do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-234">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="808b1-235">5067</span><span class="sxs-lookup"><span data-stu-id="808b1-235">5067</span></span></p></td>
<td><p><span data-ttu-id="808b1-236">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-236">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-237">Usada para solicitações SIP de entrada do gateway PSTN para o Servidor de Mediação.</span><span class="sxs-lookup"><span data-stu-id="808b1-237">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-238">Servidores Front-End que também executam um Servidor de Mediação Colocado</span><span class="sxs-lookup"><span data-stu-id="808b1-238">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="808b1-239">Serviço de mediação do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-239">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="808b1-240">5068</span><span class="sxs-lookup"><span data-stu-id="808b1-240">5068</span></span></p></td>
<td><p><span data-ttu-id="808b1-241">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-241">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-242">Usada para solicitações SIP de entrada do gateway PSTN para o Servidor de Mediação.</span><span class="sxs-lookup"><span data-stu-id="808b1-242">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-243">Servidores Front-End que também executam um Servidor de Mediação Colocado</span><span class="sxs-lookup"><span data-stu-id="808b1-243">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="808b1-244">Serviço de mediação do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-244">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="808b1-245">5081</span><span class="sxs-lookup"><span data-stu-id="808b1-245">5081</span></span></p></td>
<td><p><span data-ttu-id="808b1-246">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-246">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-247">Usada para solicitações SIP de saída do Servidor de Mediação para o gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="808b1-247">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-248">Servidores Front-End que também executam um Servidor de Mediação Colocado</span><span class="sxs-lookup"><span data-stu-id="808b1-248">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="808b1-249">Serviço de mediação do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-249">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="808b1-250">5082</span><span class="sxs-lookup"><span data-stu-id="808b1-250">5082</span></span></p></td>
<td><p><span data-ttu-id="808b1-251">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-251">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-252">Usada para solicitações SIP de saída do Servidor de Mediação para o gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="808b1-252">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-253">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-253">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-254">Serviço de compartilhamento de aplicativos do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-254">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="808b1-255">5065</span><span class="sxs-lookup"><span data-stu-id="808b1-255">5065</span></span></p></td>
<td><p><span data-ttu-id="808b1-256">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-256">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-257">Usada para solicitações de escuta do SIP de entrada para compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="808b1-257">Used for incoming SIP listening requests for application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-258">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-258">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-259">Serviço de compartilhamento de aplicativos do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-259">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="808b1-260">49152-65535</span><span class="sxs-lookup"><span data-stu-id="808b1-260">49152-65535</span></span></p></td>
<td><p><span data-ttu-id="808b1-261">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-261">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-262">Intervalo de porta de mídia usado para compartilhamento de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="808b1-262">Media port range used for application sharing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-263">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-263">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-264">Serviço de anúncio de conferência do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-264">Lync Server Conferencing Announcement service</span></span></p></td>
<td><p><span data-ttu-id="808b1-265">5073</span><span class="sxs-lookup"><span data-stu-id="808b1-265">5073</span></span></p></td>
<td><p><span data-ttu-id="808b1-266">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-266">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-267">Usado para solicitações SIP recebidas para o serviço de anúncio de conferência do Lync Server (ou seja, para conferência discada).</span><span class="sxs-lookup"><span data-stu-id="808b1-267">Used for incoming SIP requests for the Lync Server Conferencing Announcement service (that is, for dial-in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-268">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-268">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-269">Serviço de Estacionamento de Chamada do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-269">Lync Server Call Park service</span></span></p></td>
<td><p><span data-ttu-id="808b1-270">5075</span><span class="sxs-lookup"><span data-stu-id="808b1-270">5075</span></span></p></td>
<td><p><span data-ttu-id="808b1-271">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-271">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-272">Usada para solicitações SIP de entrada para o aplicativo Estacionamento de Chamadas.</span><span class="sxs-lookup"><span data-stu-id="808b1-272">Used for incoming SIP requests for the Call Park application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-273">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-273">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-274">Serviço de teste de áudio do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-274">Lync Server Audio Test service</span></span></p></td>
<td><p><span data-ttu-id="808b1-275">5076</span><span class="sxs-lookup"><span data-stu-id="808b1-275">5076</span></span></p></td>
<td><p><span data-ttu-id="808b1-276">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-276">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-277">Usada para solicitações SIP de entrada para o serviço Teste de Áudio.</span><span class="sxs-lookup"><span data-stu-id="808b1-277">Used for incoming SIP requests for the Audio Test service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-278">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-278">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-279">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="808b1-279">Not applicable</span></span></p></td>
<td><p><span data-ttu-id="808b1-280">5066</span><span class="sxs-lookup"><span data-stu-id="808b1-280">5066</span></span></p></td>
<td><p><span data-ttu-id="808b1-281">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-281">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-282">Usada para o gateway de E9-1-1 (9-1-1 Avançado) de saída.</span><span class="sxs-lookup"><span data-stu-id="808b1-282">Used for outbound Enhanced 9-1-1 (E9-1-1) gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-283">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-283">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-284">Serviço Grupo de Resposta do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-284">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="808b1-285">5071</span><span class="sxs-lookup"><span data-stu-id="808b1-285">5071</span></span></p></td>
<td><p><span data-ttu-id="808b1-286">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-286">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-287">Usada para solicitações SIP de entrada para o aplicativo Grupo de Respostas.</span><span class="sxs-lookup"><span data-stu-id="808b1-287">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-288">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-288">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-289">Serviço Grupo de Resposta do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-289">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="808b1-290">8404</span><span class="sxs-lookup"><span data-stu-id="808b1-290">8404</span></span></p></td>
<td><p><span data-ttu-id="808b1-291">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-291">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-292">Usada para solicitações SIP de entrada para o aplicativo Grupo de Respostas.</span><span class="sxs-lookup"><span data-stu-id="808b1-292">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-293">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-293">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-294">Serviço de política de largura de banda do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-294">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="808b1-295">5080</span><span class="sxs-lookup"><span data-stu-id="808b1-295">5080</span></span></p></td>
<td><p><span data-ttu-id="808b1-296">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-296">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-297">Usada para controle de admissão de chamada pelo serviço Política de Largura de banda para tráfego TURN de Borda A/V.</span><span class="sxs-lookup"><span data-stu-id="808b1-297">Used for call admission control by the Bandwidth Policy service for A/V Edge TURN traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-298">Servidores Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-298">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-299">Serviço de política de largura de banda do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-299">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="808b1-300">448</span><span class="sxs-lookup"><span data-stu-id="808b1-300">448</span></span></p></td>
<td><p><span data-ttu-id="808b1-301">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-301">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-302">Usado para controle de admissão de chamadas pelo serviço de política de largura de banda do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="808b1-302">Used for call admission control by the Lync Server Bandwidth Policy Service.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-303">Servidores front-end nos quais o repositório de gerenciamento central reside</span><span class="sxs-lookup"><span data-stu-id="808b1-303">Front End Servers where the Central Management store resides</span></span></p></td>
<td><p><span data-ttu-id="808b1-304">Serviço de agente do Lync Server Master Replicator</span><span class="sxs-lookup"><span data-stu-id="808b1-304">Lync Server Master Replicator Agent service</span></span></p></td>
<td><p><span data-ttu-id="808b1-305">445</span><span class="sxs-lookup"><span data-stu-id="808b1-305">445</span></span></p></td>
<td><p><span data-ttu-id="808b1-306">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-306">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-307">Usado para enviar por push dados de configuração do repositório de gerenciamento central para servidores que executam o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="808b1-307">Used to push configuration data from the Central Management store to servers running Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-308">Todos os servidores</span><span class="sxs-lookup"><span data-stu-id="808b1-308">All Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-309">Navegador do SQL</span><span class="sxs-lookup"><span data-stu-id="808b1-309">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="808b1-310">1434</span><span class="sxs-lookup"><span data-stu-id="808b1-310">1434</span></span></p></td>
<td><p><span data-ttu-id="808b1-311">UDP</span><span class="sxs-lookup"><span data-stu-id="808b1-311">UDP</span></span></p></td>
<td><p><span data-ttu-id="808b1-312">Navegador do SQL para cópia replicada local de dados do repositório de gerenciamento central na instância do SQL Server local</span><span class="sxs-lookup"><span data-stu-id="808b1-312">SQL Browser for local replicated copy of Central Management store data in local SQL Server instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-313">Todos os servidores internos</span><span class="sxs-lookup"><span data-stu-id="808b1-313">All internal servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-314">Vários</span><span class="sxs-lookup"><span data-stu-id="808b1-314">Various</span></span></p></td>
<td><p><span data-ttu-id="808b1-315">49152-57500</span><span class="sxs-lookup"><span data-stu-id="808b1-315">49152-57500</span></span></p></td>
<td><p><span data-ttu-id="808b1-316">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="808b1-316">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="808b1-317">Intervalo de porta de mídia usada para audioconferência em todos os servidores internos.</span><span class="sxs-lookup"><span data-stu-id="808b1-317">Media port range used for audio conferencing on all internal servers.</span></span> <span data-ttu-id="808b1-318">Usado por todos os servidores que encerram áudio: servidores front-end (para o serviço de atendedor do Lync Server Conferencing, serviço de anúncio de conferência do Lync Server e serviço de videoconferência/vídeo do Lync Server) e servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="808b1-318">Used by all servers that terminate audio: Front End Servers (for Lync Server Conferencing Attendant service, Lync Server Conferencing Announcement service, and Lync Server Audio/Video Conferencing service), and Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-319">Servidor Office Web Apps</span><span class="sxs-lookup"><span data-stu-id="808b1-319">Office Web Apps Servers</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="808b1-320">443</span><span class="sxs-lookup"><span data-stu-id="808b1-320">443</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="808b1-321">Usado pelo Lync Server 2013 para se conectar ao servidor do Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="808b1-321">Used by Lync Server 2013 to connect to Office Web Apps Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-322">Diretores</span><span class="sxs-lookup"><span data-stu-id="808b1-322">Directors</span></span></p></td>
<td><p><span data-ttu-id="808b1-323">Serviço Front-End do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-323">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="808b1-324">5060</span><span class="sxs-lookup"><span data-stu-id="808b1-324">5060</span></span></p></td>
<td><p><span data-ttu-id="808b1-325">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-325">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-326">Usada como opção para rotas estáticas até os serviços confiáveis, como servidores de controle de chamada remota.</span><span class="sxs-lookup"><span data-stu-id="808b1-326">Optionally used for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-327">Diretores</span><span class="sxs-lookup"><span data-stu-id="808b1-327">Directors</span></span></p></td>
<td><p><span data-ttu-id="808b1-328">Serviço Front-End do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-328">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="808b1-329">444</span><span class="sxs-lookup"><span data-stu-id="808b1-329">444</span></span></p></td>
<td><p><span data-ttu-id="808b1-330">HTTPS</span><span class="sxs-lookup"><span data-stu-id="808b1-330">HTTPS</span></span></p>
<p><span data-ttu-id="808b1-331">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-331">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-332">Comunicação entre servidores entre Front-End e Diretor.</span><span class="sxs-lookup"><span data-stu-id="808b1-332">Inter-server communication between Front End and Director.</span></span> <span data-ttu-id="808b1-333">Além disso, a publicação de certificado do cliente (para servidores front-end) ou a validar se o certificado do cliente já foi publicado.</span><span class="sxs-lookup"><span data-stu-id="808b1-333">Additionally, client certificate publish (to Front End Servers) or validate if the client certificate has already been published.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-334">Diretores</span><span class="sxs-lookup"><span data-stu-id="808b1-334">Directors</span></span></p></td>
<td><p><span data-ttu-id="808b1-335">Serviço de compatibilidade da Web do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-335">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="808b1-336">80</span><span class="sxs-lookup"><span data-stu-id="808b1-336">80</span></span></p></td>
<td><p><span data-ttu-id="808b1-337">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-337">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-p105">Usada para comunicação inicial dos Diretores com os FQDNs de farm da web (as URLs usadas pelos componentes da web IIS). Em uma operação normal, trocará para tráfego HTTPS, usando a porta 443 e o tipo de protocolo TCP.</span><span class="sxs-lookup"><span data-stu-id="808b1-p105">Used for initial communication from Directors to the web farm FQDNs (the URLs used by IIS web components). In normal operation, will switch to HTTPS traffic, using port 443 and protocol type TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-340">Diretores</span><span class="sxs-lookup"><span data-stu-id="808b1-340">Directors</span></span></p></td>
<td><p><span data-ttu-id="808b1-341">Serviço de compatibilidade da Web do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-341">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="808b1-342">443</span><span class="sxs-lookup"><span data-stu-id="808b1-342">443</span></span></p></td>
<td><p><span data-ttu-id="808b1-343">HTTPS</span><span class="sxs-lookup"><span data-stu-id="808b1-343">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="808b1-344">Usada para comunicação dos Diretores com os FQDNs de farm da web (as URLs usadas pelos componentes da web IIS).</span><span class="sxs-lookup"><span data-stu-id="808b1-344">Used for communication from Directors to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-345">Diretores</span><span class="sxs-lookup"><span data-stu-id="808b1-345">Directors</span></span></p></td>
<td><p><span data-ttu-id="808b1-346">Serviço Front-End do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-346">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="808b1-347">5061</span><span class="sxs-lookup"><span data-stu-id="808b1-347">5061</span></span></p></td>
<td><p><span data-ttu-id="808b1-348">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-348">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-349">Usada para comunicações internas entre os servidores e para conexões do cliente.</span><span class="sxs-lookup"><span data-stu-id="808b1-349">Used for internal communications between servers and for client connections.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-350">Servidores de mediação</span><span class="sxs-lookup"><span data-stu-id="808b1-350">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-351">Serviço de mediação do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-351">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="808b1-352">5070</span><span class="sxs-lookup"><span data-stu-id="808b1-352">5070</span></span></p></td>
<td><p><span data-ttu-id="808b1-353">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-353">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-354">Usada pelo Servidor de mediação para solicitações de entrada do Servidor Front-End.</span><span class="sxs-lookup"><span data-stu-id="808b1-354">Used by the Mediation Server for incoming requests from the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-355">Servidores de mediação</span><span class="sxs-lookup"><span data-stu-id="808b1-355">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-356">Serviço de mediação do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-356">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="808b1-357">5067</span><span class="sxs-lookup"><span data-stu-id="808b1-357">5067</span></span></p></td>
<td><p><span data-ttu-id="808b1-358">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-358">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-359">Usada para solicitações SIP de entrada do gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="808b1-359">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-360">Servidores de mediação</span><span class="sxs-lookup"><span data-stu-id="808b1-360">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-361">Serviço de mediação do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-361">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="808b1-362">5068</span><span class="sxs-lookup"><span data-stu-id="808b1-362">5068</span></span></p></td>
<td><p><span data-ttu-id="808b1-363">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-363">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-364">Usada para solicitações SIP de entrada do gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="808b1-364">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-365">Servidores de mediação</span><span class="sxs-lookup"><span data-stu-id="808b1-365">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="808b1-366">Serviço de mediação do Lync Server</span><span class="sxs-lookup"><span data-stu-id="808b1-366">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="808b1-367">5070</span><span class="sxs-lookup"><span data-stu-id="808b1-367">5070</span></span></p></td>
<td><p><span data-ttu-id="808b1-368">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-368">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-369">Usada para solicitações SIP dos Servidores Front-End.</span><span class="sxs-lookup"><span data-stu-id="808b1-369">Used for SIP requests from the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-370">Servidor de front-end de bate-papo persistente</span><span class="sxs-lookup"><span data-stu-id="808b1-370">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="808b1-371">SIP de bate-papo persistente</span><span class="sxs-lookup"><span data-stu-id="808b1-371">Persistent Chat SIP</span></span></p></td>
<td><p><span data-ttu-id="808b1-372">5041</span><span class="sxs-lookup"><span data-stu-id="808b1-372">5041</span></span></p></td>
<td><p><span data-ttu-id="808b1-373">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-373">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-374">Servidor de front-end de bate-papo persistente</span><span class="sxs-lookup"><span data-stu-id="808b1-374">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="808b1-375">Bate-papo persistente do Windows Communication Foundation (WCF)</span><span class="sxs-lookup"><span data-stu-id="808b1-375">Persistent Chat Windows Communication Foundation (WCF)</span></span></p></td>
<td><p><span data-ttu-id="808b1-376">881</span><span class="sxs-lookup"><span data-stu-id="808b1-376">881</span></span></p></td>
<td><p><span data-ttu-id="808b1-377">TCP (TLS) e TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-377">TCP (TLS) and TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-378">Servidor de front-end de bate-papo persistente</span><span class="sxs-lookup"><span data-stu-id="808b1-378">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="808b1-379">Serviço de transferência de arquivos de bate-papo persistente</span><span class="sxs-lookup"><span data-stu-id="808b1-379">Persistent Chat File Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="808b1-380">443</span><span class="sxs-lookup"><span data-stu-id="808b1-380">443</span></span></p></td>
<td><p><span data-ttu-id="808b1-381">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-381">TCP (TLS)</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="808b1-382">Alguns cenários de controle de chamada remota exigem uma conexão TCP entre o Servidor Front-End ou o Diretor e o PBX.</span><span class="sxs-lookup"><span data-stu-id="808b1-382">Some remote call control scenarios require a TCP connection between the Front End Server or Director and the PBX.</span></span> <span data-ttu-id="808b1-383">Embora o Lync Server não use mais a porta TCP 5060, durante a implantação do controle de chamada remota, você cria uma configuração de servidor confiável, que associa o FQDN do servidor de linha de RCC à porta TCP que o servidor front-end ou o diretor usará para se conectar ao sistema PBX.</span><span class="sxs-lookup"><span data-stu-id="808b1-383">Although Lync Server no longer uses TCP port 5060, during remote call control deployment you create a trusted server configuration, which associates the RCC Line Server FQDN with the TCP port that the Front End Server or Director will use to connect to the PBX system.</span></span> <span data-ttu-id="808b1-384">Para obter detalhes, consulte o cmdlet <STRONG>CsTrustedApplicationComputer</STRONG> na documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="808b1-384">For details, see the <STRONG>CsTrustedApplicationComputer</STRONG> cmdlet in the Lync Server Management Shell documentation.</span></span>



</div>

<span data-ttu-id="808b1-385">Para os seus pools que usam somente o balanceamento de carga de hardware (não o balanceamento de carga DNS), a tabela a seguir mostra as portas que precisam abrir os balanceadores de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="808b1-385">For your pools that use only hardware load balancing (not DNS load balancing), the following table shows the ports that need to open the hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-only-hardware-load-balancing"></a><span data-ttu-id="808b1-386">Portas do balanceador de carga de hardware se estiver usando somente o balanceador de carga de hardware</span><span class="sxs-lookup"><span data-stu-id="808b1-386">Hardware Load Balancer Ports if Using Only Hardware Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="808b1-387">Balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="808b1-387">Load Balancer</span></span></th>
<th><span data-ttu-id="808b1-388">Porta</span><span class="sxs-lookup"><span data-stu-id="808b1-388">Port</span></span></th>
<th><span data-ttu-id="808b1-389">Protocolo</span><span class="sxs-lookup"><span data-stu-id="808b1-389">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="808b1-390">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-390">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-391">5061</span><span class="sxs-lookup"><span data-stu-id="808b1-391">5061</span></span></p></td>
<td><p><span data-ttu-id="808b1-392">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-392">TCP (TLS)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-393">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-393">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-394">444</span><span class="sxs-lookup"><span data-stu-id="808b1-394">444</span></span></p></td>
<td><p><span data-ttu-id="808b1-395">HTTPS</span><span class="sxs-lookup"><span data-stu-id="808b1-395">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-396">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-396">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-397">135</span><span class="sxs-lookup"><span data-stu-id="808b1-397">135</span></span></p></td>
<td><p><span data-ttu-id="808b1-398">DCOM e RPC (controle de procedimento remoto)</span><span class="sxs-lookup"><span data-stu-id="808b1-398">DCOM and remote procedure call (RPC)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-399">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-399">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-400">80</span><span class="sxs-lookup"><span data-stu-id="808b1-400">80</span></span></p></td>
<td><p><span data-ttu-id="808b1-401">HTTP</span><span class="sxs-lookup"><span data-stu-id="808b1-401">HTTP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-402">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-402">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-403">8080</span><span class="sxs-lookup"><span data-stu-id="808b1-403">8080</span></span></p></td>
<td><p><span data-ttu-id="808b1-404">TCP - Recuperação por parte do cliente e do dispositivo do certificado raiz do Servidor Front-End – clientes e dispositivos autenticados por NTLM</span><span class="sxs-lookup"><span data-stu-id="808b1-404">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-405">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-405">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-406">443</span><span class="sxs-lookup"><span data-stu-id="808b1-406">443</span></span></p></td>
<td><p><span data-ttu-id="808b1-407">HTTPS</span><span class="sxs-lookup"><span data-stu-id="808b1-407">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-408">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-408">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-409">4443</span><span class="sxs-lookup"><span data-stu-id="808b1-409">4443</span></span></p></td>
<td><p><span data-ttu-id="808b1-410">HTTPS (do proxy reverso)</span><span class="sxs-lookup"><span data-stu-id="808b1-410">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-411">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-411">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-412">5072</span><span class="sxs-lookup"><span data-stu-id="808b1-412">5072</span></span></p></td>
<td><p><span data-ttu-id="808b1-413">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-413">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-414">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-414">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-415">5073</span><span class="sxs-lookup"><span data-stu-id="808b1-415">5073</span></span></p></td>
<td><p><span data-ttu-id="808b1-416">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-416">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-417">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-417">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-418">5075</span><span class="sxs-lookup"><span data-stu-id="808b1-418">5075</span></span></p></td>
<td><p><span data-ttu-id="808b1-419">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-419">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-420">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-420">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-421">5076</span><span class="sxs-lookup"><span data-stu-id="808b1-421">5076</span></span></p></td>
<td><p><span data-ttu-id="808b1-422">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-422">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-423">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-423">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-424">5071</span><span class="sxs-lookup"><span data-stu-id="808b1-424">5071</span></span></p></td>
<td><p><span data-ttu-id="808b1-425">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-425">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-426">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-426">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-427">5080</span><span class="sxs-lookup"><span data-stu-id="808b1-427">5080</span></span></p></td>
<td><p><span data-ttu-id="808b1-428">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-428">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-429">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-429">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-430">448</span><span class="sxs-lookup"><span data-stu-id="808b1-430">448</span></span></p></td>
<td><p><span data-ttu-id="808b1-431">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-431">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-432">Balanceador de carga do Servidor de mediação</span><span class="sxs-lookup"><span data-stu-id="808b1-432">Mediation Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-433">5070</span><span class="sxs-lookup"><span data-stu-id="808b1-433">5070</span></span></p></td>
<td><p><span data-ttu-id="808b1-434">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-434">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-435">Balanceador de carga do Servidor Front-End (se o pool também executa o Servidor de mediação)</span><span class="sxs-lookup"><span data-stu-id="808b1-435">Front End Server load balancer (if the pool also runs Mediation Server)</span></span></p></td>
<td><p><span data-ttu-id="808b1-436">5070</span><span class="sxs-lookup"><span data-stu-id="808b1-436">5070</span></span></p></td>
<td><p><span data-ttu-id="808b1-437">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-437">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-438">Balanceador de carga do Diretor</span><span class="sxs-lookup"><span data-stu-id="808b1-438">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-439">443</span><span class="sxs-lookup"><span data-stu-id="808b1-439">443</span></span></p></td>
<td><p><span data-ttu-id="808b1-440">HTTPS</span><span class="sxs-lookup"><span data-stu-id="808b1-440">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-441">Balanceador de carga do Diretor</span><span class="sxs-lookup"><span data-stu-id="808b1-441">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-442">444</span><span class="sxs-lookup"><span data-stu-id="808b1-442">444</span></span></p></td>
<td><p><span data-ttu-id="808b1-443">HTTPS</span><span class="sxs-lookup"><span data-stu-id="808b1-443">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-444">Balanceador de carga do Diretor</span><span class="sxs-lookup"><span data-stu-id="808b1-444">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-445">5061</span><span class="sxs-lookup"><span data-stu-id="808b1-445">5061</span></span></p></td>
<td><p><span data-ttu-id="808b1-446">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-446">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-447">Balanceador de carga do Diretor</span><span class="sxs-lookup"><span data-stu-id="808b1-447">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-448">4443</span><span class="sxs-lookup"><span data-stu-id="808b1-448">4443</span></span></p></td>
<td><p><span data-ttu-id="808b1-449">HTTPS (do proxy reverso)</span><span class="sxs-lookup"><span data-stu-id="808b1-449">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="808b1-p107">Seus pools do Front-End e do Diretor que usam o balanceamento de carga DNS também precisam ter um balanceador de carga de hardware implantado. A tabela a seguir mostra as portas que precisam ser abertas nesses balanceadores de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="808b1-p107">Your Front End pools and Director pools that use DNS load balancing also must have a hardware load balancer deployed. The following table shows the ports that need to be open on these hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-dns-load-balancing"></a><span data-ttu-id="808b1-452">Portas do balanceador de carga de hardware se estiver usando o balanceamento de carga DNS</span><span class="sxs-lookup"><span data-stu-id="808b1-452">Hardware Load Balancer Ports if Using DNS Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="808b1-453">Balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="808b1-453">Load Balancer</span></span></th>
<th><span data-ttu-id="808b1-454">Porta</span><span class="sxs-lookup"><span data-stu-id="808b1-454">Port</span></span></th>
<th><span data-ttu-id="808b1-455">Protocolo</span><span class="sxs-lookup"><span data-stu-id="808b1-455">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="808b1-456">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-456">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-457">80</span><span class="sxs-lookup"><span data-stu-id="808b1-457">80</span></span></p></td>
<td><p><span data-ttu-id="808b1-458">HTTP</span><span class="sxs-lookup"><span data-stu-id="808b1-458">HTTP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-459">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-459">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-460">443</span><span class="sxs-lookup"><span data-stu-id="808b1-460">443</span></span></p></td>
<td><p><span data-ttu-id="808b1-461">HTTPS</span><span class="sxs-lookup"><span data-stu-id="808b1-461">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-462">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-462">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-463">8080</span><span class="sxs-lookup"><span data-stu-id="808b1-463">8080</span></span></p></td>
<td><p><span data-ttu-id="808b1-464">TCP - Recuperação por parte do cliente e do dispositivo do certificado raiz do Servidor Front-End – clientes e dispositivos autenticados por NTLM</span><span class="sxs-lookup"><span data-stu-id="808b1-464">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-465">Balanceador de carga do Servidor Front-End</span><span class="sxs-lookup"><span data-stu-id="808b1-465">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-466">4443</span><span class="sxs-lookup"><span data-stu-id="808b1-466">4443</span></span></p></td>
<td><p><span data-ttu-id="808b1-467">HTTPS (do proxy reverso)</span><span class="sxs-lookup"><span data-stu-id="808b1-467">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-468">Balanceador de carga do Diretor</span><span class="sxs-lookup"><span data-stu-id="808b1-468">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-469">443</span><span class="sxs-lookup"><span data-stu-id="808b1-469">443</span></span></p></td>
<td><p><span data-ttu-id="808b1-470">HTTPS</span><span class="sxs-lookup"><span data-stu-id="808b1-470">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-471">Balanceador de carga do Diretor</span><span class="sxs-lookup"><span data-stu-id="808b1-471">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="808b1-472">4443</span><span class="sxs-lookup"><span data-stu-id="808b1-472">4443</span></span></p></td>
<td><p><span data-ttu-id="808b1-473">HTTPS (do proxy reverso)</span><span class="sxs-lookup"><span data-stu-id="808b1-473">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="required-client-ports"></a><span data-ttu-id="808b1-474">Portas do cliente necessárias</span><span class="sxs-lookup"><span data-stu-id="808b1-474">Required Client Ports</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="808b1-475">Componente</span><span class="sxs-lookup"><span data-stu-id="808b1-475">Component</span></span></th>
<th><span data-ttu-id="808b1-476">Porta</span><span class="sxs-lookup"><span data-stu-id="808b1-476">Port</span></span></th>
<th><span data-ttu-id="808b1-477">Protocolo</span><span class="sxs-lookup"><span data-stu-id="808b1-477">Protocol</span></span></th>
<th><span data-ttu-id="808b1-478">Notas</span><span class="sxs-lookup"><span data-stu-id="808b1-478">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="808b1-479">Clientes</span><span class="sxs-lookup"><span data-stu-id="808b1-479">Clients</span></span></p></td>
<td><p><span data-ttu-id="808b1-480">67/68</span><span class="sxs-lookup"><span data-stu-id="808b1-480">67/68</span></span></p></td>
<td><p><span data-ttu-id="808b1-481">DHCP</span><span class="sxs-lookup"><span data-stu-id="808b1-481">DHCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-482">Usado pelo Lync Server para localizar o FQDN do registrador (isto é, se as configurações de SRV DNS falharem e as configurações manuais não estiverem definidas).</span><span class="sxs-lookup"><span data-stu-id="808b1-482">Used by Lync Server to find the Registrar FQDN (that is, if DNS SRV fails and manual settings are not configured).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-483">Clientes</span><span class="sxs-lookup"><span data-stu-id="808b1-483">Clients</span></span></p></td>
<td><p><span data-ttu-id="808b1-484">443</span><span class="sxs-lookup"><span data-stu-id="808b1-484">443</span></span></p></td>
<td><p><span data-ttu-id="808b1-485">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-485">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-486">Usada para tráfego SIP do cliente para o servidor para acesso de usuário externo.</span><span class="sxs-lookup"><span data-stu-id="808b1-486">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-487">Clientes</span><span class="sxs-lookup"><span data-stu-id="808b1-487">Clients</span></span></p></td>
<td><p><span data-ttu-id="808b1-488">443</span><span class="sxs-lookup"><span data-stu-id="808b1-488">443</span></span></p></td>
<td><p><span data-ttu-id="808b1-489">TCP (PSOM/TLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-489">TCP (PSOM/TLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-490">Usada para acesso de usuário externo às sessões de webconferência.</span><span class="sxs-lookup"><span data-stu-id="808b1-490">Used for external user access to web conferencing sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-491">Clientes</span><span class="sxs-lookup"><span data-stu-id="808b1-491">Clients</span></span></p></td>
<td><p><span data-ttu-id="808b1-492">443</span><span class="sxs-lookup"><span data-stu-id="808b1-492">443</span></span></p></td>
<td><p><span data-ttu-id="808b1-493">TCP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="808b1-493">TCP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="808b1-494">Usada para acesso de usuário externa às sessões de A/V e mídia (TCP)</span><span class="sxs-lookup"><span data-stu-id="808b1-494">Used for external user access to A/V sessions and media (TCP)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-495">Clientes</span><span class="sxs-lookup"><span data-stu-id="808b1-495">Clients</span></span></p></td>
<td><p><span data-ttu-id="808b1-496">3478</span><span class="sxs-lookup"><span data-stu-id="808b1-496">3478</span></span></p></td>
<td><p><span data-ttu-id="808b1-497">UDP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="808b1-497">UDP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="808b1-498">Usada para acesso de usuário externo às sessões de A/V e mídia (UDP)</span><span class="sxs-lookup"><span data-stu-id="808b1-498">Used for external user access to A/V sessions and media (UDP)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-499">Clientes</span><span class="sxs-lookup"><span data-stu-id="808b1-499">Clients</span></span></p></td>
<td><p><span data-ttu-id="808b1-500">5061</span><span class="sxs-lookup"><span data-stu-id="808b1-500">5061</span></span></p></td>
<td><p><span data-ttu-id="808b1-501">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="808b1-501">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="808b1-502">Usada para tráfego SIP do cliente para o servidor para acesso de usuário externo.</span><span class="sxs-lookup"><span data-stu-id="808b1-502">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-503">Clientes</span><span class="sxs-lookup"><span data-stu-id="808b1-503">Clients</span></span></p></td>
<td><p><span data-ttu-id="808b1-504">6891-6901</span><span class="sxs-lookup"><span data-stu-id="808b1-504">6891-6901</span></span></p></td>
<td><p><span data-ttu-id="808b1-505">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-505">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-506">Usado para transferência de arquivos entre clientes do Lync e clientes anteriores (clientes do Microsoft Office Communications Server 2007 R2, Microsoft Office Communications Server 2007 e Live Communications Server 2005).</span><span class="sxs-lookup"><span data-stu-id="808b1-506">Used for file transfer between Lync clients and previous clients (clients of Microsoft Office Communications Server 2007 R2, Microsoft Office Communications Server 2007, and Live Communications Server 2005).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-507">Clientes</span><span class="sxs-lookup"><span data-stu-id="808b1-507">Clients</span></span></p></td>
<td><p><span data-ttu-id="808b1-508">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="808b1-508">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="808b1-509">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="808b1-509">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="808b1-510">Intervalo de porta de áudio (mínimo de 20 portas necessárias)</span><span class="sxs-lookup"><span data-stu-id="808b1-510">Audio port range (minimum of 20 ports required)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-511">Clientes</span><span class="sxs-lookup"><span data-stu-id="808b1-511">Clients</span></span></p></td>
<td><p><span data-ttu-id="808b1-512">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="808b1-512">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="808b1-513">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="808b1-513">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="808b1-514">Intervalo de porta de vídeo (mínimo de 20 portas necessárias).</span><span class="sxs-lookup"><span data-stu-id="808b1-514">Video port range (minimum of 20 ports required).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-515">Clientes</span><span class="sxs-lookup"><span data-stu-id="808b1-515">Clients</span></span></p></td>
<td><p><span data-ttu-id="808b1-516">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="808b1-516">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="808b1-517">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-517">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-518">Transferência de arquivos ponto a ponto (para transferência de arquivo de conferência, clientes que usam PSOM).</span><span class="sxs-lookup"><span data-stu-id="808b1-518">Peer-to-peer file transfer (for conferencing file transfer, clients use PSOM).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="808b1-519">Clientes</span><span class="sxs-lookup"><span data-stu-id="808b1-519">Clients</span></span></p></td>
<td><p><span data-ttu-id="808b1-520">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="808b1-520">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="808b1-521">TCP</span><span class="sxs-lookup"><span data-stu-id="808b1-521">TCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-522">Compartilhamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="808b1-522">Application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="808b1-523">Telefone de área comum Aastra 6721ip</span><span class="sxs-lookup"><span data-stu-id="808b1-523">Aastra 6721ip common area phone</span></span></p>
<p><span data-ttu-id="808b1-524">Telefone de mesa Aastra 6725ip</span><span class="sxs-lookup"><span data-stu-id="808b1-524">Aastra 6725ip desk phone</span></span></p>
<p><span data-ttu-id="808b1-525">Telefone IP HP 4110 (telefone de área comum)</span><span class="sxs-lookup"><span data-stu-id="808b1-525">HP 4110 IP Phone (common area phone)</span></span></p>
<p><span data-ttu-id="808b1-526">Telefone IP HP 4120 (telefone de mesa)</span><span class="sxs-lookup"><span data-stu-id="808b1-526">HP 4120 IP Phone (desk phone)</span></span></p>
<p><span data-ttu-id="808b1-527">Telefone de área comum IP Polycom CX500</span><span class="sxs-lookup"><span data-stu-id="808b1-527">Polycom CX500 IP common area phone</span></span></p>
<p><span data-ttu-id="808b1-528">Telefone de mesa IP Polycom CX600</span><span class="sxs-lookup"><span data-stu-id="808b1-528">Polycom CX600 IP desk phone</span></span></p>
<p><span data-ttu-id="808b1-529">Telefone de mesa IP Polycom CX700</span><span class="sxs-lookup"><span data-stu-id="808b1-529">Polycom CX700 IP desk phone</span></span></p>
<p><span data-ttu-id="808b1-530">Telefone de conferência IP Polycom CX3000</span><span class="sxs-lookup"><span data-stu-id="808b1-530">Polycom CX3000 IP conference phone</span></span></p></td>
<td><p><span data-ttu-id="808b1-531">67/68</span><span class="sxs-lookup"><span data-stu-id="808b1-531">67/68</span></span></p></td>
<td><p><span data-ttu-id="808b1-532">DHCP</span><span class="sxs-lookup"><span data-stu-id="808b1-532">DHCP</span></span></p></td>
<td><p><span data-ttu-id="808b1-533">Usado pelos dispositivos listados para localizar o certificado do Lync Server, o provisionamento e o FQDN do registrador.</span><span class="sxs-lookup"><span data-stu-id="808b1-533">Used by the listed devices to find the Lync Server certificate, provisioning FQDN, and Registrar FQDN.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="808b1-534">**\*** Para configurar portas específicas para esses tipos de mídia, use o cmdlet CsConferencingConfiguration (parâmetros ClientMediaPortRangeEnabled, ClientMediaPort e ClientMediaPortRange).</span><span class="sxs-lookup"><span data-stu-id="808b1-534">**\*** To configure specific ports for these media types, use the CsConferencingConfiguration cmdlet (ClientMediaPortRangeEnabled, ClientMediaPort, and ClientMediaPortRange parameters).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="808b1-535">Os programas definidos para clientes do Lync criam automaticamente as exceções necessárias de firewall do sistema operacional no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="808b1-535">The set programs for Lync clients automatically create the required operating-system firewall exceptions on the client computer.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="808b1-536">As portas usadas para acesso de usuário externo são necessárias para qualquer cenário no qual o cliente precisa atravessar o firewall da organização (por exemplo, quaisquer comunicações externas ou reuniões hospedadas por outras organizações).</span><span class="sxs-lookup"><span data-stu-id="808b1-536">The ports that are used for external user access are required for any scenario in which the client must traverse the organization’s firewall (for example, any external communications or meetings hosted by other organizations).</span></span>



<span data-ttu-id="808b1-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="808b1-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

