---
title: Configurar o servidor de mediação
description: Configurar o servidor de mediação.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configure Mediation Server
ms:assetid: 583236fd-33cd-4045-81df-baa58ed07779
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204913(v=OCS.15)
ms:contentKeyID: 48184207
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5723d9446122b85f7bd1812f7c6f411c5c1c9dbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390011"
---
# <a name="configure-mediation-server"></a><span data-ttu-id="bd8e1-103">Configurar o servidor de mediação</span><span class="sxs-lookup"><span data-stu-id="bd8e1-103">Configure Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bd8e1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bd8e1-104">

<span> </span></span></span>

<span data-ttu-id="bd8e1-105">_**Tópico da última modificação:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="bd8e1-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="bd8e1-106">Este procedimento detalha as etapas para configurar o pool do Lync Server 2013 para usar o servidor de mediação do Lync Server 2013, em vez do servidor herdado do Office Communications Server 2007 R2 Media Server.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-106">This procedure details the steps to configure the Lync Server 2013 pool to use the Lync Server 2013 Mediation Server, instead of the legacy Office Communications Server 2007 R2 Mediation Server.</span></span>

<span data-ttu-id="bd8e1-107">Para publicar, habilitar ou desabilitar uma topologia com êxito ao adicionar ou remover uma função de servidor, você deve estar conectado como um usuário que é membro do grupo RTCUniversalServerAdmins e administradores do domínio.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-107">To successfully publish, enable, or disable a topology when adding or removing a server role, you should be logged in as a user who is a member of the RTCUniversalServerAdmins and Domain Admins groups.</span></span> <span data-ttu-id="bd8e1-108">Também é possível delegar direitos e permissões de administrador adequadas para adicionar funções de servidor.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-108">It is also possible to delegate the proper administrator rights and permissions for adding server roles.</span></span> <span data-ttu-id="bd8e1-109">Para obter detalhes, consulte delegar permissões de configuração na documentação de implantação do servidor Standard Edition ou Enterprise Edition Server.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-109">For details, see Delegate Setup Permissions in the Standard Edition server or Enterprise Edition server Deployment documentation.</span></span> <span data-ttu-id="bd8e1-110">Para outras alterações de configuração, somente a associação no grupo RTCUniversalServerAdmins é necessária.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-110">For other configuration changes, only membership in the RTCUniversalServerAdmins group is required.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bd8e1-111">Para obter as informações mais recentes sobre como localizar gateways PSTN qualificados, PBXs IP e serviços de entroncamento SIP que funcionam com o Lync Server 2013, consulte "programa de interoperabilidade aberto da Microsoft Unified Communications" em <A href="https://go.microsoft.com/fwlink/p/?linkid=206015">https://go.microsoft.com/fwlink/p/?linkId=206015</A> .</span><span class="sxs-lookup"><span data-stu-id="bd8e1-111">For the latest information on finding qualified PSTN gateways, IP-PBXs, and SIP trunking services that work with Lync Server 2013, see "Microsoft Unified Communications Open Interoperability Program" at <A href="https://go.microsoft.com/fwlink/p/?linkid=206015">https://go.microsoft.com/fwlink/p/?linkId=206015</A>.</span></span>



</div>

<div>

## <a name="to-configure-mediation-server-using-topology-builder"></a><span data-ttu-id="bd8e1-112">Para configurar o servidor de mediação usando o construtor de topologias</span><span class="sxs-lookup"><span data-stu-id="bd8e1-112">To configure Mediation Server Using Topology Builder</span></span>

1.  <span data-ttu-id="bd8e1-113">Abra uma topologia existente do construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-113">Open an existing topology from Topology Builder.</span></span>

2.  <span data-ttu-id="bd8e1-114">No painel esquerdo, navegue até **gateways PSTN**.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-114">In the left pane, navigate to **PSTN gateways**.</span></span>

3.  <span data-ttu-id="bd8e1-115">Clique com o botão direito do mouse em **gateways PSTN** e clique em **novo gateway IP/PSTN**.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-115">Right-click **PSTN gateways**, and then click **New IP/PSTN Gateway**.</span></span>

4.  <span data-ttu-id="bd8e1-116">Conclua a página **definir o novo gateway IP/PSTN** com as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="bd8e1-116">Complete the **Define New IP/PSTN Gateway** page with the following information:</span></span>
    
      - <span data-ttu-id="bd8e1-117">Digite o endereço IP ou FQDN do gateway.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-117">Enter the gateway FQDN or IP address.</span></span> <span data-ttu-id="bd8e1-118">O FQDN do gateway será necessário se o gateway usar o protocolo TLS.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-118">The FQDN of the gateway is required if the gateway uses the TLS protocol.</span></span>
    
      - <span data-ttu-id="bd8e1-119">Aceite o valor padrão da **porta de escuta do gateway IP/PSTN** ou digite a nova porta de escuta se ela tiver sido modificada.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-119">Accept the default value of the **Listening port for IP/PSTN gateway** or enter the new listening port if it was modified.</span></span>
    
      - <span data-ttu-id="bd8e1-120">Defina o **protocolo de transporte SIP**.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-120">Set the **Sip Transport Protocol**.</span></span>

5.  <span data-ttu-id="bd8e1-121">No painel esquerdo, navegue até o **pool de front-end do Enterprise Edition** ou o **servidor Standard Edition**.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-121">In the left pane, navigate to the **Enterprise Edition Front End pool** or the **Standard Edition Server**.</span></span>

6.  <span data-ttu-id="bd8e1-122">Clique com o botão direito do mouse no pool e, em seguida, clique em **Editar propriedades**.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-122">Right-click the pool, and then click **Edit Properties**.</span></span>

7.  <span data-ttu-id="bd8e1-123">Em **servidor de mediação**, defina as **portas de escuta**.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-123">Under **Mediation Server**, set the **Listening ports**.</span></span>

8.  <span data-ttu-id="bd8e1-124">Em seguida, associe o gateway PSTN recém-criado selecionando-o e clicando em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-124">Next, associate the newly created PSTN gateway by selecting it and clicking **Add**.</span></span>

9.  <span data-ttu-id="bd8e1-125">Em **Construtor de topologia**, selecione o nó mais superior do **Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-125">In **Topology Builder**, select the top-most node **Lync Server**.</span></span>

10. <span data-ttu-id="bd8e1-126">No menu **ação** , selecione **publicar topologia** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-126">From the **Action** menu, select **Publish Topology** and then click **Next**.</span></span>

11. <span data-ttu-id="bd8e1-127">Quando o **Assistente de publicação** for concluído, clique em **concluir** para fechar o assistente.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-127">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bd8e1-128">É importante que você conclua o próximo tópico, <A href="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md">altere as rotas de voz para usar o novo servidor de mediação do Lync server 2013</A> para garantir que as rotas de voz aponte para o servidor de mediação correto.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-128">It is important that you complete the next topic, <A href="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md">Change voice routes to use the new Lync Server 2013 Mediation Server</A> to ensure that the voice routes are pointing to the correct Mediation Server.</span></span>



<span data-ttu-id="bd8e1-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bd8e1-129"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

