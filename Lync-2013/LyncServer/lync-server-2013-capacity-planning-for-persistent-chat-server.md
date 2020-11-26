---
title: 'Lync Server 2013: planejamento de capacidade para servidor de chat persistente'
description: 'Lync Server 2013: planejamento de capacidade para servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Persistent Chat Server
ms:assetid: 7a850cd5-c789-4795-a8ff-083be21ae784
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615006(v=OCS.15)
ms:contentKeyID: 48184580
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f78f9f3666fb272b808ef36da2d3010f451d0079
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435555"
---
# <a name="capacity-planning-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="0c4f3-103">Planejamento de capacidade para servidor de chat persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c4f3-103">Capacity planning for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0c4f3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0c4f3-104">

<span> </span></span></span>

<span data-ttu-id="0c4f3-105">_**Tópico da última modificação:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="0c4f3-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="0c4f3-106">O servidor de chat persistente pode executar chats em tempo real de vários usuários que podem persistir para recuperação futura e pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-106">Persistent Chat Server can perform multi-user real-time chat that can persist for future retrieval and search.</span></span> <span data-ttu-id="0c4f3-107">Ao contrário das mensagens instantâneas em grupo (IM) salvas na caixa de correio de um usuário, se o histórico da conversa estiver configurado, uma sessão persistente do servidor de chat permanecerá aberta, e o conteúdo será salvo em um servidor, juntamente com as mensagens, arquivos, URLs e outros dados que fazem parte de uma conversa em andamento.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-107">Unlike group instant messaging (IM) that is saved in a user’s mailbox if conversation history is configured, a Persistent Chat Server session stays open longer, and the content is saved on a server, along with the messages, files, URLs, and other data that are part of an ongoing conversation.</span></span>

<span data-ttu-id="0c4f3-108">O planejamento de capacidade é uma parte importante da preparação para a implantação do servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-108">Capacity planning is an important part of preparing to deploy Persistent Chat Server.</span></span> <span data-ttu-id="0c4f3-109">Este tópico fornece detalhes sobre topologias persistentes de servidor de chat com suporte e tabelas de planejamento de capacidade que você pode usar para determinar a melhor configuração para a sua implantação.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-109">This topic provides details about supported Persistent Chat Server topologies and capacity planning tables that you can use to determine the best configuration for your deployment.</span></span> <span data-ttu-id="0c4f3-110">Ele também descreve como gerenciar melhor implantações persistentes do servidor de chat que exigem maior capacidade nos horários de pico.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-110">It also describes how to best manage Persistent Chat Server deployments that require greater capacity at peak times.</span></span>

<span data-ttu-id="0c4f3-111">Para baixar o servidor de chat persistente, consulte "servidor de chat persistente do Microsoft Lync Server 13" em [https://go.microsoft.com/fwlink/p/?linkId=209539](https://go.microsoft.com/fwlink/p/?linkid=209539) .</span><span class="sxs-lookup"><span data-stu-id="0c4f3-111">To download Persistent Chat Server, see "Microsoft Lync Server 13 Persistent Chat Server" at [https://go.microsoft.com/fwlink/p/?linkId=209539](https://go.microsoft.com/fwlink/p/?linkid=209539).</span></span>

<span data-ttu-id="0c4f3-112">Para obter detalhes sobre como instalar o servidor de chat persistente, consulte [instalando o servidor de chat persistente no Lync Server 2013](lync-server-2013-installing-persistent-chat-server.md) e [Configurando o servidor de chat persistente no Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-112">For details about installing Persistent Chat Server, see [Installing Persistent Chat Server in Lync Server 2013](lync-server-2013-installing-persistent-chat-server.md) and [Configuring Persistent Chat Server in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="0c4f3-113">Ferramentas de suporte, como o Lync Server Planning Tool, podem ajudá-lo ainda mais no planejamento da capacidade.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-113">Support tools, such as Lync Server Planning Tool, can further assist you with capacity planning.</span></span> <span data-ttu-id="0c4f3-114">Para obter detalhes sobre a ferramenta de planejamento, consulte [iniciando o processo de planejamento do Lync Server 2013](lync-server-2013-beginning-the-planning-process.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-114">For details about the Planning Tool, see [Beginning the planning process for Lync Server 2013](lync-server-2013-beginning-the-planning-process.md) in the Planning documentation.</span></span>

<div>

## <a name="persistent-chat-server-supported-topologies"></a><span data-ttu-id="0c4f3-115">Topologias compatíveis com o servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="0c4f3-115">Persistent Chat Server Supported Topologies</span></span>

<span data-ttu-id="0c4f3-116">Você pode implantar um servidor de chat persistente em pools de servidor único ou de vários servidores e com topologia de pool único ou de vários pools.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-116">You can deploy Persistent Chat Server in single-server or multiple-server pools, and with single-pool or multiple-pool topology.</span></span>

<span data-ttu-id="0c4f3-117">Agora também é compatível com o servidor de chat persistente no servidor Standard Edition para novas implantações do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-117">We now also support Persistent Chat Server on Standard Edition server for new Lync Server 2013 deployments.</span></span> <span data-ttu-id="0c4f3-118">No entanto, o desempenho e a escala serão afetados, e como não há uma opção de alta disponibilidade para esta nova implantação, esperamos que você o use principalmente para fins de prova de conceito, avaliação e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-118">However, performance and scale will be affected, and because there is no high availability option for this new deployment, we expect you to use this primarily for the purposes of proof of concept, evaluation, and so on.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0c4f3-119">Para obter detalhes adicionais sobre ambas as topologias, consulte <A href="lync-server-2013-planning-for-persistent-chat-server.md">planejando o servidor de chat persistente no Lync server 2013</A> neste conjunto de documentação e <A href="lync-server-2013-deploying-persistent-chat-server.md">implantando o servidor de chat persistente no Lync Server 2013</A> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-119">For additional details about both topologies, see <A href="lync-server-2013-planning-for-persistent-chat-server.md">Planning for Persistent Chat Server in Lync Server 2013</A> in this documentation set and <A href="lync-server-2013-deploying-persistent-chat-server.md">Deploying Persistent Chat Server in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="single-server-topology"></a><span data-ttu-id="0c4f3-120">Single-Server topologia</span><span class="sxs-lookup"><span data-stu-id="0c4f3-120">Single-Server Topology</span></span>

<span data-ttu-id="0c4f3-121">A configuração mínima e a implantação mais simples para o servidor de chat persistente é uma única topologia de servidor front-end persistente do servidor de chat.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-121">The minimum configuration and simplest deployment for Persistent Chat Server is a single Persistent Chat Server Front End Server topology.</span></span> <span data-ttu-id="0c4f3-122">Esta implantação requer um único servidor que executa o servidor de chat persistente (que, opcionalmente, executa o serviço de conformidade, se a conformidade estiver habilitada), um servidor que hospede o banco de dados do SQL Server e se a conformidade for necessária, o banco de dados do SQL Server para armazenar os dados de conformidade.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-122">This deployment requires a single server that runs Persistent Chat Server (which optionally runs the Compliance service, if compliance is enabled), a server that hosts both the SQL Server database, and if compliance is required, the SQL Server database to store the compliance data.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="0c4f3-123">Você não pode adicionar mais servidores a um pool de servidores de chat persistente iniciado como uma implantação de servidor único no construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-123">You cannot add additional servers to a Persistent Chat Server pool that is started as a single-server deployment in Topology Builder.</span></span> <span data-ttu-id="0c4f3-124">Recomendamos usar a topologia de pool de vários servidores, mesmo se você estiver usando um único servidor.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-124">We recommend using the multiple-server pool topology, even if you’re using a single server.</span></span> <span data-ttu-id="0c4f3-125">Isso é possível para que você possa adicionar mais servidores mais tarde, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-125">This is so that you’ll be able to add more servers later, if it's necessary.</span></span> 


</div>

<span data-ttu-id="0c4f3-126">A figura a seguir mostra todos os componentes obrigatórios e opcionais de uma topologia para um único servidor de front-end do servidor de chat persistente com conformidade.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-126">The following figure shows all required and optional components of a topology for a single Persistent Chat Server Front End Server with compliance.</span></span>

<span data-ttu-id="0c4f3-127">**Único servidor de chat persistente**</span><span class="sxs-lookup"><span data-stu-id="0c4f3-127">**Single Persistent Chat Server**</span></span>

<span data-ttu-id="0c4f3-128">![Topologia de servidor único com serviço de conformidade](images/Gg398500.9168fa52-61e0-4d17-a14d-45fd32e81456(OCS.15).jpg "Topologia de servidor único com serviço de conformidade")</span><span class="sxs-lookup"><span data-stu-id="0c4f3-128">![Single server topology with Compliance service](images/Gg398500.9168fa52-61e0-4d17-a14d-45fd32e81456(OCS.15).jpg "Single server topology with Compliance service")</span></span>

</div>

<div>

## <a name="multiple-server-topology"></a><span data-ttu-id="0c4f3-129">Multiple-Server topologia</span><span class="sxs-lookup"><span data-stu-id="0c4f3-129">Multiple-Server Topology</span></span>

<span data-ttu-id="0c4f3-130">Para fornecer maior capacidade e confiabilidade, você pode implantar uma topologia de vários servidores, conforme descrito em [planejamento para servidor de chat persistente no Lync server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="0c4f3-130">To provide greater capacity and reliability, you can deploy a multiple-server topology, as described in [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span></span> <span data-ttu-id="0c4f3-131">A topologia de vários servidores pode incluir até quatro computadores ativos que executam o servidor de chat persistente (as configurações de alta disponibilidade e recuperação de desastres permitirão até oito, mas apenas quatro podem estar ativas e as quatro restantes em standby).</span><span class="sxs-lookup"><span data-stu-id="0c4f3-131">The multiple-server topology can include as many as four active computers running Persistent Chat Server (high availability and disaster recovery configurations will allow up to eight, but only four can be active and the remaining four on standby).</span></span> <span data-ttu-id="0c4f3-132">Cada servidor pode oferecer suporte a quantos usuários simultâneos do 20.000, para um total de 80.000 usuários simultâneos conectados a um pool de servidores de chat persistente com quatro servidores.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-132">Each server can support as many as 20,000 concurrent users, for a total of 80,000 concurrent users connected to a Persistent Chat Server pool with 4 servers.</span></span> <span data-ttu-id="0c4f3-133">Uma topologia de vários servidores é a mesma que a topologia de servidor único, exceto que vários servidores hospedam o servidor de chat persistente e podem ser dimensionados para maior.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-133">A multiple-server topology is the same as the single-server topology except that multiple servers host Persistent Chat Server, and can scale higher.</span></span> <span data-ttu-id="0c4f3-134">Vários computadores que executam o servidor de chat persistente devem residir no mesmo domínio dos serviços de domínio Active Directory do Lync Server e no serviço de conformidade.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-134">Multiple computers running Persistent Chat Server should reside in the same Active Directory Domain Services domain as Lync Server and the Compliance service.</span></span>

<span data-ttu-id="0c4f3-135">A figura a seguir mostra todos os componentes de uma topologia de vários servidores com vários computadores que executam o servidor de chat persistente, o serviço de conformidade opcional e um banco de dados de conformidade separado.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-135">The following figure shows all the components of a multiple-server topology with multiple computers running Persistent Chat Server, the optional Compliance service, and a separate compliance database.</span></span>

<span data-ttu-id="0c4f3-136">**Vários servidores de chat persistentes**</span><span class="sxs-lookup"><span data-stu-id="0c4f3-136">**Multiple Persistent Chat Servers**</span></span>

<span data-ttu-id="0c4f3-137">![Topologia de vários servidores](images/Gg398500.19aea898-28df-4d9b-903c-f72ef062d919(OCS.15).jpg "Topologia de vários servidores")</span><span class="sxs-lookup"><span data-stu-id="0c4f3-137">![Multiple server topology](images/Gg398500.19aea898-28df-4d9b-903c-f72ef062d919(OCS.15).jpg "Multiple server topology")</span></span>

<span data-ttu-id="0c4f3-138">Em uma implantação de servidor de chat persistente de quatro servidores, em que os usuários do 80.000 podem ser conectados simultaneamente e usar chats persistentes, a carga é distribuída uniformemente em 20.000 usuários por servidor.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-138">In a four-server Persistent Chat Server deployment, where 80,000 users can be simultaneously signed in to and using Persistent Chat, the load is distributed evenly at 20,000 users per server.</span></span> <span data-ttu-id="0c4f3-139">Se um servidor ficar indisponível, os usuários que estiverem conectados a esse servidor perderão o acesso ao servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-139">If one server becomes unavailable, the users who are connected to that server will lose their access to Persistent Chat Server.</span></span> <span data-ttu-id="0c4f3-140">Os usuários desconectados serão automaticamente transferidos para os servidores remanescentes até que o servidor indisponível seja restaurado.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-140">The disconnected users will be automatically transferred to the remaining servers until the unavailable server is restored.</span></span> <span data-ttu-id="0c4f3-141">Dependendo da quantidade de tráfego de chat persistente na rede, esta transferência pode demorar alguns minutos ou mais.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-141">Depending on the amount of Persistent Chat traffic on the network, this transfer can take a few minutes or longer.</span></span> <span data-ttu-id="0c4f3-142">Como cada um dos servidores restantes pode estar hospedando tantos quanto os usuários do 30.000, recomendamos que você restaure o servidor indisponível o mais rápido possível para evitar problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-142">Because each of the remaining servers might be hosting as many as 30,000 users, we recommend that you restore the unavailable server as quickly as possible to avoid performance issues.</span></span> <span data-ttu-id="0c4f3-143">Caso contrário, você pode disponibilizar outro servidor de chat persistente usando o construtor de topologias ou o cmdlet do Windows PowerShell, **set-CsPersistentChatActiveServer**.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-143">Otherwise, you can make another Persistent Chat Server available by using the Topology Builder or the Windows PowerShell cmdlet, **set-CsPersistentChatActiveServer**.</span></span>

</div>

</div>

<div>

## <a name="persistent-chat-server-capacity-planning"></a><span data-ttu-id="0c4f3-144">Planejamento da capacidade do servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="0c4f3-144">Persistent Chat Server Capacity Planning</span></span>

<span data-ttu-id="0c4f3-145">As tabelas a seguir podem ajudá-lo com o planejamento da capacidade para o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-145">The following tables can help you with capacity planning for Persistent Chat Server.</span></span> <span data-ttu-id="0c4f3-146">Eles modelam como alterar várias configurações de servidor de chat persistente afetam os recursos de capacidade.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-146">They model how changing various Persistent Chat Server settings affect capacity capabilities.</span></span>

<div>

## <a name="planning-your-maximum-capacity-for-persistent-chat-server"></a><span data-ttu-id="0c4f3-147">Planejando a capacidade máxima para o servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="0c4f3-147">Planning Your Maximum Capacity for Persistent Chat Server</span></span>

<span data-ttu-id="0c4f3-148">Use a seguinte tabela de exemplo para determinar o número de usuários que você será capaz de suportar.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-148">Use the following sample table to determine the number of users you will be able to support.</span></span>

### <a name="persistent-chat-server-pool-maximum-capacity-sample"></a><span data-ttu-id="0c4f3-149">Exemplo de capacidade máxima do pool do servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="0c4f3-149">Persistent Chat Server pool Maximum Capacity Sample</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-150">Instâncias ativas do serviço de chat persistente</span><span class="sxs-lookup"><span data-stu-id="0c4f3-150">Active Persistent Chat service instances</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-151"><em>4</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-151"><em>4</em></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-152">Instâncias do serviço de chat persistente</span><span class="sxs-lookup"><span data-stu-id="0c4f3-152">Persistent Chat service instances</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-153"><em>8 (4 deve estar inativo; somente um máximo de 4 pode estar ativo)</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-153"><em>8 (4 must be inactive; only a maximum of 4 can be active)</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-154">Usuários ativos conectados</span><span class="sxs-lookup"><span data-stu-id="0c4f3-154">Active users connected</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-155"><em>80,000</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-155"><em>80,000</em></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-156">Total de usuários provisionados</span><span class="sxs-lookup"><span data-stu-id="0c4f3-156">Total provisioned users</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-157">150,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-157">150,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-158">Número de pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="0c4f3-158">Number of endpoints</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-159">120,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-159">120,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0c4f3-160">No exemplo anterior, o plano é compatível com o número máximo de usuários que o chat do servidor de chat persistente permite: quatro servidores/instâncias do serviço de chat persistente (pode ter quatro servidores passivos executando o servidor de chat persistente para alta disponibilidade e recuperação de desastres) e os usuários do 20.000 por servidor, para um total de 80.000 usuários ativos.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-160">In the preceding sample, the plan is to support the maximum number of users that Persistent Chat Server allows: four servers/instances of the Persistent Chat service (can have four more passive servers running Persistent Chat Server for high availability and disaster recovery) and 20,000 users per server, for a total of 80,000 active users.</span></span>

</div>

<div>

## <a name="capacity-planning-for-managing-persistent-chat-room-access"></a><span data-ttu-id="0c4f3-161">Planejamento de capacidade para gerenciar o acesso persistente à sala de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-161">Capacity Planning for Managing Persistent Chat Room Access</span></span>

<span data-ttu-id="0c4f3-162">A tabela de exemplo a seguir pode ajudá-lo a planejar o gerenciamento de acesso à sala de chat persistente em um pool de servidores de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-162">The following sample table can help you plan for managing Persistent Chat room access in a Persistent Chat Server pool.</span></span>

### <a name="managing-chat-room-access-sample"></a><span data-ttu-id="0c4f3-163">Como gerenciar o exemplo de acesso à sala de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-163">Managing Chat Room Access Sample</span></span>

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
<th></th>
<th><span data-ttu-id="0c4f3-164">Salas de chat pequenas</span><span class="sxs-lookup"><span data-stu-id="0c4f3-164">Small Chat Rooms</span></span></th>
<th><span data-ttu-id="0c4f3-165">Salas de chat médias</span><span class="sxs-lookup"><span data-stu-id="0c4f3-165">Medium Chat Rooms</span></span></th>
<th><span data-ttu-id="0c4f3-166">Salas de chat grandes</span><span class="sxs-lookup"><span data-stu-id="0c4f3-166">Large Chat Rooms</span></span></th>
<th><span data-ttu-id="0c4f3-167">Total</span><span class="sxs-lookup"><span data-stu-id="0c4f3-167">Total</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-168">Tamanho das salas de chat (número de usuários conectados)</span><span class="sxs-lookup"><span data-stu-id="0c4f3-168">Size of chat rooms (number of users connected)</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-169">30 por sala</span><span class="sxs-lookup"><span data-stu-id="0c4f3-169">30 per room</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-170">150 por sala</span><span class="sxs-lookup"><span data-stu-id="0c4f3-170">150 per room</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-171">16.000 por sala</span><span class="sxs-lookup"><span data-stu-id="0c4f3-171">16,000 per room</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-172">Salas de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-172">Chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-173">32,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-173">32,000</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-174">1,067</span><span class="sxs-lookup"><span data-stu-id="0c4f3-174">1,067</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-175">254</span><span class="sxs-lookup"><span data-stu-id="0c4f3-175">10</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-176">33,077</span><span class="sxs-lookup"><span data-stu-id="0c4f3-176">33,077</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-177">% de salas que são auditórios</span><span class="sxs-lookup"><span data-stu-id="0c4f3-177">% of rooms that are auditorium</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-178">1%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-178">1%</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-179">1%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-179">1%</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-180">50%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-180">50%</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-181">% de salas abertas</span><span class="sxs-lookup"><span data-stu-id="0c4f3-181">% of rooms that are open</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-182">3%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-182">3%</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-183">3%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-183">3%</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-184">50%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-184">50%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-185">Salas abertas (para associação explícita)</span><span class="sxs-lookup"><span data-stu-id="0c4f3-185">Open rooms (no explicit membership)</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-186">960</span><span class="sxs-lookup"><span data-stu-id="0c4f3-186">960</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-187">32</span><span class="sxs-lookup"><span data-stu-id="0c4f3-187">32</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-188">5</span><span class="sxs-lookup"><span data-stu-id="0c4f3-188">5</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-189">997</span><span class="sxs-lookup"><span data-stu-id="0c4f3-189">997</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-190">Salas não abertas (salas normais com associação explícita)</span><span class="sxs-lookup"><span data-stu-id="0c4f3-190">Non-open rooms (regular rooms with explicit membership)</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-191">31,040</span><span class="sxs-lookup"><span data-stu-id="0c4f3-191">31,040</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-192">1.035</span><span class="sxs-lookup"><span data-stu-id="0c4f3-192">1.035</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-193">5</span><span class="sxs-lookup"><span data-stu-id="0c4f3-193">5</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-194">32,080</span><span class="sxs-lookup"><span data-stu-id="0c4f3-194">32,080</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-195">Salas de auditório (ingresso de apresentadores adicionais)</span><span class="sxs-lookup"><span data-stu-id="0c4f3-195">Auditorium rooms (additional presenters entry)</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-196">0</span><span class="sxs-lookup"><span data-stu-id="0c4f3-196">0</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-197">32</span><span class="sxs-lookup"><span data-stu-id="0c4f3-197">32</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-198">5</span><span class="sxs-lookup"><span data-stu-id="0c4f3-198">5</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-199">Salas gerenciadas pro associação direta</span><span class="sxs-lookup"><span data-stu-id="0c4f3-199">Rooms managed by direct membership</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-200">50%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-200">50%</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-201">10%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-201">10%</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-202">0%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-202">0%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-203">Salas gerenciadas por grupos de usuários</span><span class="sxs-lookup"><span data-stu-id="0c4f3-203">Rooms managed by user groups</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-204">50%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-204">50%</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-205">90%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-205">90%</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-206">100%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-206">100%</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-207">Grupos de usuários na lista de associação de cada sala de chat para salas abertas (sem especificação explícita)</span><span class="sxs-lookup"><span data-stu-id="0c4f3-207">User groups in each chat room's membership list for open rooms (not specified explicitly)</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-208">0</span><span class="sxs-lookup"><span data-stu-id="0c4f3-208">0</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-209">0</span><span class="sxs-lookup"><span data-stu-id="0c4f3-209">0</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-210">0</span><span class="sxs-lookup"><span data-stu-id="0c4f3-210">0</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-211">Usuários na lista de associação de cada sala de chat para salas não abertas</span><span class="sxs-lookup"><span data-stu-id="0c4f3-211">Users in each chat room's membership list for non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-212">30</span><span class="sxs-lookup"><span data-stu-id="0c4f3-212">30</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-213">150</span><span class="sxs-lookup"><span data-stu-id="0c4f3-213">150</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-214">16,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-214">16,000</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-215">Grupos de usuários na lista de associação de cada sala de chat para salas não abertas</span><span class="sxs-lookup"><span data-stu-id="0c4f3-215">User groups in each chat room's membership list for non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-216">3</span><span class="sxs-lookup"><span data-stu-id="0c4f3-216">3</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-217">5</span><span class="sxs-lookup"><span data-stu-id="0c4f3-217">5</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-218">254</span><span class="sxs-lookup"><span data-stu-id="0c4f3-218">10</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-219">Usuários e grupos de usuários na lista de gerentes de cada sala de chat (para salas abertas e não abertas)</span><span class="sxs-lookup"><span data-stu-id="0c4f3-219">Users and user groups in each chat room's manager list (for open and non-open rooms)</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-220">6</span><span class="sxs-lookup"><span data-stu-id="0c4f3-220">6</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-221">6</span><span class="sxs-lookup"><span data-stu-id="0c4f3-221">6</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-222">6</span><span class="sxs-lookup"><span data-stu-id="0c4f3-222">6</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-223">Usuários e grupos de usuários na lista de apresentadores de cada sala de chat (para salas abertas e não abertas)</span><span class="sxs-lookup"><span data-stu-id="0c4f3-223">Users and user groups in each auditorium chat room's presenters list (for open and non-open rooms)</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-224">6</span><span class="sxs-lookup"><span data-stu-id="0c4f3-224">6</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-225">6</span><span class="sxs-lookup"><span data-stu-id="0c4f3-225">6</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-226">6</span><span class="sxs-lookup"><span data-stu-id="0c4f3-226">6</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-227">Entidades de associação com base em usuário em todas as salas não abertas</span><span class="sxs-lookup"><span data-stu-id="0c4f3-227">User-based membership entities across all non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-228">465,600</span><span class="sxs-lookup"><span data-stu-id="0c4f3-228">465,600</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-229">15,520</span><span class="sxs-lookup"><span data-stu-id="0c4f3-229">15,520</span></span></p></td>
<td><p>-</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-230">Entidades de associação com base em grupo usuários em todas as salas não abertas</span><span class="sxs-lookup"><span data-stu-id="0c4f3-230">User-group-based membership entities across all non-open rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-231">46,560</span><span class="sxs-lookup"><span data-stu-id="0c4f3-231">46,560</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-232">4656</span><span class="sxs-lookup"><span data-stu-id="0c4f3-232">4656</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-233">50</span><span class="sxs-lookup"><span data-stu-id="0c4f3-233">50</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-234">Entidades de usuários e grupos de usuários em todas as salas de chat de auditório</span><span class="sxs-lookup"><span data-stu-id="0c4f3-234">Users and user groups based entities across all auditorium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-235">0</span><span class="sxs-lookup"><span data-stu-id="0c4f3-235">0</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-236">192</span><span class="sxs-lookup"><span data-stu-id="0c4f3-236">192</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-237">50</span><span class="sxs-lookup"><span data-stu-id="0c4f3-237">50</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-238">Entidades de gerente com base em usuários e grupos de usuários em todas as listas de gerentes das salas de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-238">Users and user groups based manager entities across all chat rooms manager lists</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-239">192,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-239">192,000</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-240">6,400</span><span class="sxs-lookup"><span data-stu-id="0c4f3-240">6,400</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-241">60</span><span class="sxs-lookup"><span data-stu-id="0c4f3-241">60</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-242">Usuários ativos por sala de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-242">Active users per chat room</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-243"><em>30</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-243"><em>30</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-244"><em>150</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-244"><em>150</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-245"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-245"><em>16,000</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-246">Salas de chat por usuário</span><span class="sxs-lookup"><span data-stu-id="0c4f3-246">Chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-247"><em>12</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-247"><em>12</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-248"><em>2</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-248"><em>2</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-249"><em>2</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-249"><em>2</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-250"><em>16</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-250"><em>16</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-251">Grupos de usuário na lista de membros de cada sala de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-251">User groups in each chat room’s membership list</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-252"><em>254</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-252"><em>10</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-253"><em>254</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-253"><em>10</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-254"><em>15</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-254"><em>15</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-255">Salas gerenciadas por grupos de usuários</span><span class="sxs-lookup"><span data-stu-id="0c4f3-255">Rooms managed by user groups</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-256"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-256"><em>50%</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-257"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-257"><em>50%</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-258"><em>50%</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-258"><em>50%</em></span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-259">Entidades de participação baseadas em grupos de usuário em todas as salas de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-259">User-group-based membership entities across all chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-260">155,200</span><span class="sxs-lookup"><span data-stu-id="0c4f3-260">155,200</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-261">5173</span><span class="sxs-lookup"><span data-stu-id="0c4f3-261">5173</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-262">68</span><span class="sxs-lookup"><span data-stu-id="0c4f3-262">68</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-263">Entidades de participação baseadas em usuários em todas as salas de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-263">User-based membership entities across all chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-264">465,600</span><span class="sxs-lookup"><span data-stu-id="0c4f3-264">465,600</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-265">77,600</span><span class="sxs-lookup"><span data-stu-id="0c4f3-265">77,600</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-266">72,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-266">72,000</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-267">Usuários e grupos de usuários no gerenciador de cada sala de chat, apresentador e listas de escopo</span><span class="sxs-lookup"><span data-stu-id="0c4f3-267">Users and user groups in each chat room's manager, presenter, and scope lists</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-268">6</span><span class="sxs-lookup"><span data-stu-id="0c4f3-268">6</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-269">6</span><span class="sxs-lookup"><span data-stu-id="0c4f3-269">6</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-270">6</span><span class="sxs-lookup"><span data-stu-id="0c4f3-270">6</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-271">Usuários e grupos de usuários em todas as listas de escopo, gerentes e apresentadores das salas de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-271">Users and user groups across all chat rooms' manager, presenter, and scope lists</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-272">192,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-272">192,000</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-273">6400</span><span class="sxs-lookup"><span data-stu-id="0c4f3-273">6400</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-274">60</span><span class="sxs-lookup"><span data-stu-id="0c4f3-274">60</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-275">Entradas de controle de acesso</span><span class="sxs-lookup"><span data-stu-id="0c4f3-275">Access control entries</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-276">704,160</span><span class="sxs-lookup"><span data-stu-id="0c4f3-276">704,160</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-277">26,768</span><span class="sxs-lookup"><span data-stu-id="0c4f3-277">26,768</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-278">160</span><span class="sxs-lookup"><span data-stu-id="0c4f3-278">160</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-279">731,088</span><span class="sxs-lookup"><span data-stu-id="0c4f3-279">731,088</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-280">Entradas de controle de máximo acesso</span><span class="sxs-lookup"><span data-stu-id="0c4f3-280">Maximum access control entries</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="0c4f3-281">2,000,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-281">2,000,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0c4f3-282">No exemplo anterior, quando você implanta os servidores de chat persistente de acordo com as diretrizes recomendadas, eles podem manipular até 80.000 usuários ativos em um pool de quatro servidores com conformidade habilitada.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-282">In the preceding sample, when you deploy the Persistent Chat Servers according to the recommended guidelines, they can handle up to 80,000 active users across a four-server pool with compliance enabled.</span></span>

<span data-ttu-id="0c4f3-283">Este exemplo mostra como salas de chat são categorizadas como pequenas (30 usuários ativos a qualquer momento), médias (150 usuários ativos) e grandes (16.000 usuários ativos).</span><span class="sxs-lookup"><span data-stu-id="0c4f3-283">This sample shows chat rooms categorized as small (30 active users at any given time), medium (150 active users), and large (16,000 active users).</span></span> <span data-ttu-id="0c4f3-284">O número de salas de chat de um determinado tamanho é calculado com base no número total de:</span><span class="sxs-lookup"><span data-stu-id="0c4f3-284">The number of chat rooms of a certain size is computed based on the total number of:</span></span>

  - <span data-ttu-id="0c4f3-285">Usuários ativos no sistema</span><span class="sxs-lookup"><span data-stu-id="0c4f3-285">Active users in the system</span></span>

  - <span data-ttu-id="0c4f3-286">Usuários ativos em salas de chat de determinado tamanho</span><span class="sxs-lookup"><span data-stu-id="0c4f3-286">Active users in chat rooms of the given size</span></span>

  - <span data-ttu-id="0c4f3-287">Salas de chat de um tamanho determinado onde ingressa um único usuário</span><span class="sxs-lookup"><span data-stu-id="0c4f3-287">Chat rooms of the given size that a single user joins</span></span>

<span data-ttu-id="0c4f3-p111">Para cada sala de chat, a tabela de planejamento de capacidade anterior especifica o número de entradas de controle de acesso que estão associados com a sala de chat, incluindo entradas que são atribuídos diretamente para a sala de chat. Você pode controlar o acesso a salas de chat individuais usando listas de controle de acesso (ACLs). Você também pode controlar o acesso no nível de categoria. Em uma ACL, uma entrada de controle de acesso individual pode ser um grupo de usuários (por exemplo, um grupo de segurança, uma lista de distribuição) ou um único usuário. Você pode definir as entradas de controle de acesso aos membros, aos apresentadores e aos gerentes de sala de chat.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-p111">For each chat room, the preceding capacity planning table specifies the number of access control entries that are associated with the chat room, including entries that are assigned directly to the chat room. You can control access to individual chat rooms by using access control lists (ACLs). You can also control access at the category level. In an ACL, an individual access control entry can be either a user group—for example, a security group, a distribution list, or a single user. You can define access control entries for chat room managers, presenters, and members.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="0c4f3-p112">No planejamento da estratégia de gerenciamento de salas de chat, tenha em mente que o número total de entradas de controle de acesso permitido é de dois milhões. Se as entradas de controle de acesso calculado excederem dois milhões, o desempenho do servidor pode degradar significativamente. Para evitar esse problema, sempre que possível, verifique se as entradas de controle de acesso são grupos de usuários em vez de usuários individuais.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-p112">In planning your strategy for managing chat rooms, keep in mind that the total number of allowed access control entries is 2 million. If the calculated access control entries exceed 2 million, server performance could degrade significantly. To avoid this issue, whenever possible, be sure that your access control entries are user groups instead of individual users.</span></span>



</div>

</div>

<div>

## <a name="capacity-planning-for-managing-chat-room-access-by-invitation"></a><span data-ttu-id="0c4f3-296">Planejamento de capacidade para gerenciar o acesso à sala de chat por convite</span><span class="sxs-lookup"><span data-stu-id="0c4f3-296">Capacity Planning for Managing Chat Room Access by Invitation</span></span>

<span data-ttu-id="0c4f3-297">Você pode usar a tabela de planejamento de capacidade a seguir para compreender o número de convites que o servidor de chat persistente cria e armazena no banco de dados de chat persistente quando ele está configurado para enviar convites.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-297">You can use the following capacity planning table to understand the number of invitations that Persistent Chat Server creates and stores in the Persistent Chat database when it is configured to send invitations.</span></span> <span data-ttu-id="0c4f3-298">Você gerencia os convites na categoria usando a página de **configurações de categoria da sala de chat** no painel de controle do Lync Server, ou usando o cmdlet do Windows PowerShell, **set-csPersistentChatCategory**.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-298">You manage invitations on the Category by using the **Chat Room Category settings** page in the Lync Server Control Panel, or by using the Windows PowerShell cmdlet, **set-csPersistentChatCategory**.</span></span> <span data-ttu-id="0c4f3-299">Você pode gerenciar convites em uma sala de chat (em linha com o que a categoria permite) usando a página de **Gerenciamento de salas** iniciada do cliente do Lync ou usando um cmdlet do Windows PowerShell, **set-csPersistentChatRoom**.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-299">You can manage invitations on a chat room (in line with what the category allows) by using the **Room Management** page launched from the Lync client, or by using a Windows PowerShell cmdlet, **set-csPersistentChatRoom**.</span></span>

<span data-ttu-id="0c4f3-300">Os dados de exemplo na tabela a seguir pressupõem que, na página de  **configurações de sala de chat** para 50% de todas as salas de chat, a opção de  **convites** está definida como  **Sim**.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-300">The sample data in the following table assumes that, on the **Chat room settings** page for 50 percent of all chat rooms, the **Invitations** option is set to **Yes**.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="0c4f3-301">Se o valor calculado para o número de convites gerado pelo servidor exceder 1 milhão, o desempenho do servidor pode degradar significativamente.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-301">If the calculated value for the number of invitations that is generated by the server exceeds 1 million, server performance could degrade significantly.</span></span> <span data-ttu-id="0c4f3-302">Para evitar esse problema, certifique-se de minimizar o número de salas de chat que estão configuradas para enviar convites ou restringir o número de usuários que podem participar de salas de chat que foram configurados para enviar convites.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-302">To avoid this issue, be sure that you minimize the number of chat rooms that are configured to send invitations or restrict the number of users who can join chat rooms that have been configured to send invitations.</span></span>



</div>

### <a name="chat-room-access-by-invitation-sample"></a><span data-ttu-id="0c4f3-303">Exemplo de acesso à sala de chat por convite</span><span class="sxs-lookup"><span data-stu-id="0c4f3-303">Chat Room Access by Invitation Sample</span></span>

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
<th></th>
<th><span data-ttu-id="0c4f3-304">Salas de chat pequenas</span><span class="sxs-lookup"><span data-stu-id="0c4f3-304">Small Chat Rooms</span></span></th>
<th><span data-ttu-id="0c4f3-305">Salas de chat médias</span><span class="sxs-lookup"><span data-stu-id="0c4f3-305">Medium Chat Rooms</span></span></th>
<th><span data-ttu-id="0c4f3-306">Salas de chat grandes</span><span class="sxs-lookup"><span data-stu-id="0c4f3-306">Large Chat Rooms</span></span></th>
<th><span data-ttu-id="0c4f3-307">Total</span><span class="sxs-lookup"><span data-stu-id="0c4f3-307">Total</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-308">Usuários que podem acessar a sala de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-308">Users who can access chat room</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-309">30 por sala</span><span class="sxs-lookup"><span data-stu-id="0c4f3-309">30 per room</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-310">150 por sala</span><span class="sxs-lookup"><span data-stu-id="0c4f3-310">150 per room</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-311">16.000 por sala</span><span class="sxs-lookup"><span data-stu-id="0c4f3-311">16,000 per room</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-312">Porcentagem de salas com convites</span><span class="sxs-lookup"><span data-stu-id="0c4f3-312">Percentage of rooms that have invitations</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-313">50%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-313">50%</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-314">50%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-314">50%</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-315">50%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-315">50%</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-316">Salas de chat configuradas para enviar convites</span><span class="sxs-lookup"><span data-stu-id="0c4f3-316">Chat rooms configured to send invitations</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-317"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-317"><em>16,000</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-318"><em>533</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-318"><em>533</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-319"><em>5</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-319"><em>5</em></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-320">Usuários que podem acessar a sala de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-320">Users who can access the chat room</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-321"><em>60</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-321"><em>60</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-322"><em>225</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-322"><em>225</em></span></span></p></td>
<td><p><span data-ttu-id="0c4f3-323"><em>16,000</em></span><span class="sxs-lookup"><span data-stu-id="0c4f3-323"><em>16,000</em></span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-324">Convites gerados pelo servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="0c4f3-324">Invitations generated by Persistent Chat Server</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-325">960,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-325">960,000</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-326">120,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-326">120,000</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-327">80,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-327">80,000</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-328">1,160,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-328">1,160,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-329">Número de convites máximo permitido</span><span class="sxs-lookup"><span data-stu-id="0c4f3-329">Maximum allowable number of invitations</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td><p><span data-ttu-id="0c4f3-330">2,000,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-330">2,000,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-331">Modelo 1 - Iniciar com o número esperado de mensagens por sala/dia</span><span class="sxs-lookup"><span data-stu-id="0c4f3-331">Model 1 - Start with expected number of messages per room per day</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-332">Taxa de chat por sala (por dia)</span><span class="sxs-lookup"><span data-stu-id="0c4f3-332">Chat Rate Per Room (per day)</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-333">50</span><span class="sxs-lookup"><span data-stu-id="0c4f3-333">50</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-334">500</span><span class="sxs-lookup"><span data-stu-id="0c4f3-334">500</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-335">100</span><span class="sxs-lookup"><span data-stu-id="0c4f3-335">100</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-336">650</span><span class="sxs-lookup"><span data-stu-id="0c4f3-336">650</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-337">Taxa de chat (por segundo) em todas as salas</span><span class="sxs-lookup"><span data-stu-id="0c4f3-337">Chat rate (per second) across all rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-338">55.56</span><span class="sxs-lookup"><span data-stu-id="0c4f3-338">55.56</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-339">18.52</span><span class="sxs-lookup"><span data-stu-id="0c4f3-339">18.52</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-340">0.03</span><span class="sxs-lookup"><span data-stu-id="0c4f3-340">0.03</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-341">74</span><span class="sxs-lookup"><span data-stu-id="0c4f3-341">74</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-342">Modelo 2 - Iniciar com um número de mensagens publicadas por usuário/dia</span><span class="sxs-lookup"><span data-stu-id="0c4f3-342">Model 2 - Start with number of messages posted per user per day</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-343">Taxa de chat por usuário/dia</span><span class="sxs-lookup"><span data-stu-id="0c4f3-343">Chat rate per user per day</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-344">15</span><span class="sxs-lookup"><span data-stu-id="0c4f3-344">15</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-345">5</span><span class="sxs-lookup"><span data-stu-id="0c4f3-345">5</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-346">0.1</span><span class="sxs-lookup"><span data-stu-id="0c4f3-346">0.1</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-347">cedido</span><span class="sxs-lookup"><span data-stu-id="0c4f3-347">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-348">Taxa de chat por sala (por dia)</span><span class="sxs-lookup"><span data-stu-id="0c4f3-348">Chat rate per room (per day)</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-349">38</span><span class="sxs-lookup"><span data-stu-id="0c4f3-349">38</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-350">375</span><span class="sxs-lookup"><span data-stu-id="0c4f3-350">375</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-351">800</span><span class="sxs-lookup"><span data-stu-id="0c4f3-351">800</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-352">1,213</span><span class="sxs-lookup"><span data-stu-id="0c4f3-352">1,213</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-353">Taxa de chat (por segundo) em todas as salas</span><span class="sxs-lookup"><span data-stu-id="0c4f3-353">Chat rate (per second) across all rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-354">41.67</span><span class="sxs-lookup"><span data-stu-id="0c4f3-354">41.67</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-355">13.89</span><span class="sxs-lookup"><span data-stu-id="0c4f3-355">13.89</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-356">0.28</span><span class="sxs-lookup"><span data-stu-id="0c4f3-356">0.28</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-357">56</span><span class="sxs-lookup"><span data-stu-id="0c4f3-357">56</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="persistent-chat-server-performance-user-model"></a><span data-ttu-id="0c4f3-358">Modelo de usuário de desempenho persistente do servidor de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-358">Persistent Chat Server Performance User Model</span></span>

<span data-ttu-id="0c4f3-359">A tabela a seguir descreve o modelo de usuário para o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-359">The following table describes the user model for Persistent Chat Server.</span></span> <span data-ttu-id="0c4f3-360">Ela fornece a base para requisitos de planejamento de capacidade e representa uma organização típica com 80.000 usuários simultâneos em quatro servidores.</span><span class="sxs-lookup"><span data-stu-id="0c4f3-360">It provides the basis for the capacity planning requirements and represents a typical organization with 80,000 concurrent users on four servers.</span></span>

### <a name="persistent-chat-server-performance-user-model"></a><span data-ttu-id="0c4f3-361">Modelo de usuário de desempenho persistente do servidor de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-361">Persistent Chat Server Performance User Model</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-362">Número de usuários ativos conectados</span><span class="sxs-lookup"><span data-stu-id="0c4f3-362">Number of active users connected</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-363">80,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-363">80,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-364">Número de instâncias de serviço do servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="0c4f3-364">Number of Persistent Chat Server service instances</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-365">4</span><span class="sxs-lookup"><span data-stu-id="0c4f3-365">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-366">Tamanho de salas de chat pequenas</span><span class="sxs-lookup"><span data-stu-id="0c4f3-366">Size of small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-367">30 usuários</span><span class="sxs-lookup"><span data-stu-id="0c4f3-367">30 users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-368">Tamanho médio de salas de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-368">Size of medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-369">150 usuários</span><span class="sxs-lookup"><span data-stu-id="0c4f3-369">150 users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-370">Tamanho grande de salas de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-370">Size of large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-371">16.000 usuários</span><span class="sxs-lookup"><span data-stu-id="0c4f3-371">16,000 users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-372">Número total de salas de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-372">Total number of chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-373">33,077</span><span class="sxs-lookup"><span data-stu-id="0c4f3-373">33,077</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-374">Número de salas de chat pequenas</span><span class="sxs-lookup"><span data-stu-id="0c4f3-374">Number of small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-375">32,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-375">32,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-376">Número de salas de chat médias</span><span class="sxs-lookup"><span data-stu-id="0c4f3-376">Number of medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-377">1,067</span><span class="sxs-lookup"><span data-stu-id="0c4f3-377">1,067</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-378">Número de salas de chat grandes</span><span class="sxs-lookup"><span data-stu-id="0c4f3-378">Number of large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-379">254</span><span class="sxs-lookup"><span data-stu-id="0c4f3-379">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-380">Número total de salas de chat por usuário</span><span class="sxs-lookup"><span data-stu-id="0c4f3-380">Total number of chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-381">16</span><span class="sxs-lookup"><span data-stu-id="0c4f3-381">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-382">Número de salas de chat pequenas por usuário</span><span class="sxs-lookup"><span data-stu-id="0c4f3-382">Number of small chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-383">12</span><span class="sxs-lookup"><span data-stu-id="0c4f3-383">12</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-384">Número de salas de chat médias por usuário</span><span class="sxs-lookup"><span data-stu-id="0c4f3-384">Number of medium chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-385">2</span><span class="sxs-lookup"><span data-stu-id="0c4f3-385">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-386">Número de salas de chat grandes por usuário</span><span class="sxs-lookup"><span data-stu-id="0c4f3-386">Number of large chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-387">2</span><span class="sxs-lookup"><span data-stu-id="0c4f3-387">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-388">Número de salas com ingresso por usuário</span><span class="sxs-lookup"><span data-stu-id="0c4f3-388">Number of rooms joined per user</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-389">24</span><span class="sxs-lookup"><span data-stu-id="0c4f3-389">24</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-390">Taxa de pico de associação</span><span class="sxs-lookup"><span data-stu-id="0c4f3-390">Peak join rate</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-391">10/segundo</span><span class="sxs-lookup"><span data-stu-id="0c4f3-391">10/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-392">Taxa de chat total</span><span class="sxs-lookup"><span data-stu-id="0c4f3-392">Total chat rate</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-393">24/segundo</span><span class="sxs-lookup"><span data-stu-id="0c4f3-393">24/second</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-394">Taxa de chat para pequenas salas de chat</span><span class="sxs-lookup"><span data-stu-id="0c4f3-394">Chat rate for small chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-395">22.22/second</span><span class="sxs-lookup"><span data-stu-id="0c4f3-395">22.22/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-396">Taxa de chat para salas de chat médias</span><span class="sxs-lookup"><span data-stu-id="0c4f3-396">Chat rate for medium chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-397">1.67/second</span><span class="sxs-lookup"><span data-stu-id="0c4f3-397">1.67/second</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-398">Taxa de chat para salas de chat grandes</span><span class="sxs-lookup"><span data-stu-id="0c4f3-398">Chat rate for large chat rooms</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-399">~0.15/second</span><span class="sxs-lookup"><span data-stu-id="0c4f3-399">~0.15/second</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-400">Porcentagem de salas de chat configuradas para convites</span><span class="sxs-lookup"><span data-stu-id="0c4f3-400">Percentage of chat rooms configured for invitations</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-401">50%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-401">50%</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-402">Porcentagem de participação direta em</span><span class="sxs-lookup"><span data-stu-id="0c4f3-402">Percentage of direct memberships</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-403">50%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-403">50%</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-404">Porcentagem de membros em grupo</span><span class="sxs-lookup"><span data-stu-id="0c4f3-404">Percentage of group memberships</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-405">50%</span><span class="sxs-lookup"><span data-stu-id="0c4f3-405">50%</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-406">Número médio de afiliações ancestrais nos serviços de domínio Active Directory</span><span class="sxs-lookup"><span data-stu-id="0c4f3-406">Average number of ancestor affiliations in Active Directory Domain Services</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-407">100 - 200</span><span class="sxs-lookup"><span data-stu-id="0c4f3-407">100 - 200</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-408">Número de contatos inscritos por usuário</span><span class="sxs-lookup"><span data-stu-id="0c4f3-408">Number of subscribed contacts per user</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-409">80</span><span class="sxs-lookup"><span data-stu-id="0c4f3-409">80</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-410">Número médio de pontos de extremidade por usuário</span><span class="sxs-lookup"><span data-stu-id="0c4f3-410">Average number of endpoints per user</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-411">1.5</span><span class="sxs-lookup"><span data-stu-id="0c4f3-411">1.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-412">Número médio de salas de chat visíveis por ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="0c4f3-412">Average number of visible chat rooms per endpoint</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-413">1.5</span><span class="sxs-lookup"><span data-stu-id="0c4f3-413">1.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-414">Número médio de salas de chat visíveis por usuário</span><span class="sxs-lookup"><span data-stu-id="0c4f3-414">Average number of visible chat rooms per user</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-415">2,25 (50% para uma sala e 50% para duas salas); até seis salas abertas, uma por monitor</span><span class="sxs-lookup"><span data-stu-id="0c4f3-415">2.25 (50% for 1 room and 50% for 2 rooms); Up to 6 rooms open, one per monitor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-416">Número de participantes sondados por intervalo</span><span class="sxs-lookup"><span data-stu-id="0c4f3-416">Number of participants polled per interval</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-417">25 por sala de chat visível</span><span class="sxs-lookup"><span data-stu-id="0c4f3-417">25 per visible chat room</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-418">Duração do intervalo de sondagem</span><span class="sxs-lookup"><span data-stu-id="0c4f3-418">Length of polling interval</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-419">5 minutos</span><span class="sxs-lookup"><span data-stu-id="0c4f3-419">5 minutes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-420">Número de participantes sondados por segundo</span><span class="sxs-lookup"><span data-stu-id="0c4f3-420">Number of participants polled per second</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-421">15,000</span><span class="sxs-lookup"><span data-stu-id="0c4f3-421">15,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c4f3-422">Número de alterações de presença por hora por usuário</span><span class="sxs-lookup"><span data-stu-id="0c4f3-422">Number of presence changes per hour per user</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-423">6</span><span class="sxs-lookup"><span data-stu-id="0c4f3-423">6</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c4f3-424">Número de alterações de presença por segundo</span><span class="sxs-lookup"><span data-stu-id="0c4f3-424">Number of presence changes per second</span></span></p></td>
<td><p><span data-ttu-id="0c4f3-425">133.33</span><span class="sxs-lookup"><span data-stu-id="0c4f3-425">133.33</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0c4f3-426">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0c4f3-426">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

