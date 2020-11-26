---
title: Exibir aplicativos de servidor do Idioma de Processamento SIP da Microsoft
description: Exibir aplicativos do servidor Microsoft SIP Processing Language (MSPL).
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View Microsoft SIP Processing Language (MSPL) server applications
ms:assetid: b7df1323-b6bd-4925-8fe6-5241c91fe51b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182575(v=OCS.15)
ms:contentKeyID: 48185202
ms.date: 09/26/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d844acf542546a668c4fc086a07cd6a7bb4a8f5a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446282"
---
# <a name="view-microsoft-sip-processing-language-mspl-server-applications-in-lync-server-2013"></a><span data-ttu-id="83f58-103">Exibir aplicativos de servidor do Idioma de Processamento SIP da Microsoft (MSPL) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="83f58-103">View Microsoft SIP Processing Language (MSPL) server applications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="83f58-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="83f58-104">

<span> </span></span></span>

<span data-ttu-id="83f58-105">_**Tópico da última modificação:** 2014-09-26_</span><span class="sxs-lookup"><span data-stu-id="83f58-105">_**Topic Last Modified:** 2014-09-26_</span></span>

<span data-ttu-id="83f58-106">Um aplicativo de servidor Microsoft SIP Processing Language (MSPL) é um aplicativo somente de script que usa uma linguagem de script em vez da API do Microsoft Lync 2010.</span><span class="sxs-lookup"><span data-stu-id="83f58-106">A Microsoft SIP Processing Language (MSPL) server application is a script-only application that uses a scripting language instead of the Microsoft Lync 2010 API.</span></span> <span data-ttu-id="83f58-107">O MSPL fornece controle mais granular sobre filtragem e comportamentos de proxy, além de um recurso para a expedição de mensagens específicas para aplicativos SIP baseados em transações.</span><span class="sxs-lookup"><span data-stu-id="83f58-107">MSPL provides more granular control over filtering and proxy behaviors, in addition to a facility for dispatching specific messages to transaction-based SIP applications.</span></span> <span data-ttu-id="83f58-108">MSPL é usado especificamente para filtrar e rotear mensagens SIP.</span><span class="sxs-lookup"><span data-stu-id="83f58-108">MSPL is used specifically for filtering and routing SIP messages.</span></span> <span data-ttu-id="83f58-109">Os aplicativos do MSPL são executados no mesmo processo do módulo userservices, enquanto um programa baseado na API do Lync 2010 é executado em um processo separado.</span><span class="sxs-lookup"><span data-stu-id="83f58-109">MSPL applications run in the same process as the UserServices module, while a program that is based on the Lync 2010 API runs in a separate process.</span></span>

<span data-ttu-id="83f58-110">Você pode usar a página de **aplicativo do servidor** no grupo **Topology** do painel de controle do Lync Server para ver uma lista de aplicativos do MSPL Server que são executados em servidores front-end no ambiente do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="83f58-110">You can use the **Server Application** page in the **Topology** group of Lync Server Control Panel to see a list of MSPL server applications that run on Front End Servers in your Lync Server 2013 environment.</span></span> <span data-ttu-id="83f58-111">A lista mostra os scripts que estão disponíveis para cada pool, bem como se eles estão habilitados ou críticos.</span><span class="sxs-lookup"><span data-stu-id="83f58-111">The list shows the scripts that are available for each pool, as well as whether they are enabled or critical.</span></span> <span data-ttu-id="83f58-112">Os scripts são executados na ordem em que são listados.</span><span class="sxs-lookup"><span data-stu-id="83f58-112">The scripts run in the order they are listed.</span></span>

<span data-ttu-id="83f58-113">Esses scripts incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="83f58-113">These scripts include the following:</span></span>

  - <span data-ttu-id="83f58-114">O ClientVersionFilter fornece ao administrador uma maneira de especificar a versão dos clientes que recebem suporte de um pool.</span><span class="sxs-lookup"><span data-stu-id="83f58-114">ClientVersionFilter provides the administrator with a way to specify the version of clients that are supported by a pool.</span></span> <span data-ttu-id="83f58-115">O filtro de versão do cliente verifica a versão do cliente e pode impedir o cliente de fazer logon ou apresentar ao usuário uma mensagem que indica que ele está usando um cliente sem suporte.</span><span class="sxs-lookup"><span data-stu-id="83f58-115">The client version filter checks the client version and can either prevent the client from logging on or present the user with a message that indicates he or she is using a client that is not supported.</span></span> <span data-ttu-id="83f58-116">O filtro de versão do cliente também pode ser configurado para exibir uma mensagem para o usuário que contém a URL da versão mais recente para download do cliente.</span><span class="sxs-lookup"><span data-stu-id="83f58-116">The client version filter can also be configured to display a message to the user that contains the URL of the latest downloadable version of the client.</span></span>

  - <span data-ttu-id="83f58-117">O TranslationService converte um número que um usuário disca para um número E. 164 de acordo com as regras de normalização definidas pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="83f58-117">TranslationService translates a number that a user dials to an E.164 number according to the normalization rules defined by the administrator.</span></span> <span data-ttu-id="83f58-118">Para obter detalhes, consulte [regras de tradução no Lync Server 2013](lync-server-2013-translation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="83f58-118">For details, see [Translation rules in Lync Server 2013](lync-server-2013-translation-rules.md).</span></span>

  - <span data-ttu-id="83f58-119">IncomingFederation impõe a validação de Federação em nível de locatário para mensagens de entrada e entre locatários de implantações externas.</span><span class="sxs-lookup"><span data-stu-id="83f58-119">IncomingFederation enforces tenant-level federation validation for inter-tenant and incoming messages from external deployments.</span></span>

  - <span data-ttu-id="83f58-120">Userservices é o componente de registrador de SIP, presença e conferência de um servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="83f58-120">UserServices is the SIP Registrar, presence, and conferencing component of a Front End Server.</span></span> <span data-ttu-id="83f58-121">Ele fornece recursos de chat, presença e conferência intimamente integrados, criados no topo do proxy SIP.</span><span class="sxs-lookup"><span data-stu-id="83f58-121">It provides closely integrated IM, presence, and conferencing features built on top of the SIP Proxy.</span></span>

  - <span data-ttu-id="83f58-122">InterClusterRouting é responsável por direcionar chamadas para o pool de registradores primários do chamador.</span><span class="sxs-lookup"><span data-stu-id="83f58-122">InterClusterRouting is responsible for routing calls to the callee’s primary Registrar pool.</span></span> <span data-ttu-id="83f58-123">Para obter detalhes, consulte [componentes de VoIP do servidor front-end para o Lync Server 2013](lync-server-2013-front-end-server-voip-components.md).</span><span class="sxs-lookup"><span data-stu-id="83f58-123">For details, see [Front End Server VoIP components for Lync Server 2013](lync-server-2013-front-end-server-voip-components.md).</span></span>

  - <span data-ttu-id="83f58-124">O IIMFilter (filtro de IM inteligente) bloqueia as mensagens que contêm URLs clicáveis ou que tentam iniciar transferências de arquivo.</span><span class="sxs-lookup"><span data-stu-id="83f58-124">IIMFilter (Intelligent IM Filter) blocks messages that contain clickable URLs or that attempt to initiate file transfers.</span></span> <span data-ttu-id="83f58-125">O IIMFilter também verifica a versão do cliente em nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="83f58-125">IIMFilter also checks the client version on behalf of the server.</span></span> <span data-ttu-id="83f58-126">IIMFilter afeta as transferências de arquivo iniciadas usando o Lync Server ou o Communicator.</span><span class="sxs-lookup"><span data-stu-id="83f58-126">IIMFilter affects file transfers that are initiated by using either Lync Server or Communicator.</span></span> <span data-ttu-id="83f58-127">Por padrão, os links clicáveis são desativados adicionando-se um caractere de sublinhado antes do primeiro caractere do link.</span><span class="sxs-lookup"><span data-stu-id="83f58-127">By default, clickable links are disabled by adding an underscore character before the first character of the link.</span></span> <span data-ttu-id="83f58-128">Um administrador pode alterar esse comportamento para que o link seja bloqueado, e, nesse caso, as mensagens que contêm URLs clicáveis ou que tentam iniciar uma transferência de arquivo são bloqueadas pelo servidor para atingir seus destinos pretendidos.</span><span class="sxs-lookup"><span data-stu-id="83f58-128">An administrator can change this behavior so that the link is blocked, in which case messages that contain clickable URLs or that attempt to initiate a file transfer are blocked by the server from reaching their intended destinations.</span></span> <span data-ttu-id="83f58-129">O IIMFilter é instalado em todos os servidores que executam o Lync Server, exceto servidores proxy e servidores de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="83f58-129">IIMFilter is installed on all servers running Lync Server except Proxy Servers and Archiving Servers.</span></span>

  - <span data-ttu-id="83f58-130">UserPinService é usado para verificar os números de identificação pessoal do usuário (PINs) para conferência discada.</span><span class="sxs-lookup"><span data-stu-id="83f58-130">UserPinService is used to verify user personal identification numbers (PINs) for dial-in conferencing.</span></span>

  - <span data-ttu-id="83f58-131">Defaultrouting é o aplicativo de roteamento padrão para servidores que executam o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="83f58-131">DefaultRouting is the default routing application for servers running Lync Server.</span></span> <span data-ttu-id="83f58-132">Ele é habilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="83f58-132">It is enabled by default.</span></span> <span data-ttu-id="83f58-133">O aplicativo de roteamento é instalado em todos os servidores Standard Edition e Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="83f58-133">The routing application is installed on all Standard Edition and Enterprise Edition servers.</span></span>

  - <span data-ttu-id="83f58-134">O ExumRouting roteia chamadas para o Exchange Server Unified Messaging (UM).</span><span class="sxs-lookup"><span data-stu-id="83f58-134">ExumRouting routes calls to Exchange Server Unified Messaging (UM).</span></span> <span data-ttu-id="83f58-135">O ExumRouting determina o servidor do Exchange UM apropriado para direcionar a chamada quando houver uma nova mensagem de caixa postal para o depósito.</span><span class="sxs-lookup"><span data-stu-id="83f58-135">ExumRouting determines the appropriate Exchange UM server to route the call to when there is a new voice mail message to deposit.</span></span> <span data-ttu-id="83f58-136">O ExumRouting também manipula alguns outros aspectos de integração do Exchange UM, incluindo o roteamento para o atendedor automático e o acesso ao Assinante.</span><span class="sxs-lookup"><span data-stu-id="83f58-136">ExumRouting also handles some other Exchange UM integration aspects, including routing to Auto Attendant and Subscriber Access.</span></span>

  - <span data-ttu-id="83f58-137">OutboundRouting determina o gateway que roteia uma chamada para um número de telefone de acordo com o número discado e a autorização de discagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="83f58-137">OutboundRouting determines the gateway that routes a call to a phone number according to the dialed number and the user’s dialing authorization.</span></span> <span data-ttu-id="83f58-138">O OutboundRouting também manipula o redirecionamento de chamadas se um gateway não puder processar uma chamada.</span><span class="sxs-lookup"><span data-stu-id="83f58-138">OutboundRouting also handles rerouting of calls if a gateway cannot process a call.</span></span>

  - <span data-ttu-id="83f58-139">QoEAgent recebe relatórios de dados de qualidade da experiência (QoE) de pontos de extremidade por meio de solicitações de serviço SIP e envia os dados para a fila de destino no servidor de monitoramento ou para consumidores de terceiros usando HTTP POST.</span><span class="sxs-lookup"><span data-stu-id="83f58-139">QoEAgent receives Quality of Experience (QoE) data reports from endpoints through SIP SERVICE requests, and sends the data to the destination queue on the Monitoring Server or to third-party consumers using HTTP POST.</span></span> <span data-ttu-id="83f58-140">Para obter detalhes, consulte [implantando o monitoramento no Lync Server 2013](lync-server-2013-deploying-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="83f58-140">For details, see [Deploying monitoring in Lync Server 2013](lync-server-2013-deploying-monitoring.md).</span></span>

  - <span data-ttu-id="83f58-141">OutgoingFederation impõe a validação de Federação em nível de locatário para mensagens indo para uma implantação externa direcionada.</span><span class="sxs-lookup"><span data-stu-id="83f58-141">OutgoingFederation enforces tenant-level federation validation for messages going to a targeted external deployment.</span></span>

  - <span data-ttu-id="83f58-142">Os proxies AcpRouting INVITEem solicitações destinadas para o provedor de serviços de audioconferência ao gateway do provedor de serviços de audioconferência.</span><span class="sxs-lookup"><span data-stu-id="83f58-142">AcpRouting proxies INVITE requests destined for the audio conferencing provider to the audio conferencing provider gateway.</span></span>

<span data-ttu-id="83f58-143">Os scripts executados em servidores de borda incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="83f58-143">Scripts that run on Edge Servers include the following:</span></span>

  - <span data-ttu-id="83f58-144">IIMFilter</span><span class="sxs-lookup"><span data-stu-id="83f58-144">IIMFilter</span></span>

  - <span data-ttu-id="83f58-145">OptionsHandler responderá às solicitações de entrada com o **200 OK** se a solicitação for destinada para o servidor atual.</span><span class="sxs-lookup"><span data-stu-id="83f58-145">OptionsHandler responds to incoming OPTIONS requests with **200 OK** if the request is destined for the current server.</span></span> <span data-ttu-id="83f58-146">Isso é usado para a validação de topologia.</span><span class="sxs-lookup"><span data-stu-id="83f58-146">This is used for topology validation.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="83f58-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="83f58-147">See Also</span></span>


[<span data-ttu-id="83f58-148">Habilitar ou desabilitar um aplicativo de servidor Microsoft SIP Processing Language (MSPL) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="83f58-148">Enable or disable a Microsoft SIP Processing Language (MSPL) server application in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-a-microsoft-sip-processing-language-mspl-server-application.md)  
[<span data-ttu-id="83f58-149">Marcar um aplicativo Microsoft SIP Processing Language (MSPL) como crítico ou não crítico no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="83f58-149">Mark a Microsoft SIP Processing Language (MSPL) application as critical or not critical in Lync Server 2013</span></span>](lync-server-2013-mark-a-microsoft-sip-processing-language-mspl-application-as-critical-or-not-critical.md)  
  

<span data-ttu-id="83f58-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="83f58-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

