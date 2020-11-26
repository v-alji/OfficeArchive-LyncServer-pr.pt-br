---
title: 'Lync Server 2013: configurar um tronco sem bypass de mídia'
description: 'Lync Server 2013: configurar um tronco sem bypass de mídia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a trunk without media bypass
ms:assetid: 3422e93e-7bd2-4470-968c-dc38345b18ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425831(v=OCS.15)
ms:contentKeyID: 48183825
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 586ab4f283034c94bd7cb0179d73a963cad88347
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434158"
---
# <a name="configure-a-trunk-without-media-bypass-in-lync-server-2013"></a><span data-ttu-id="e2997-103">Configurar um tronco sem bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2997-103">Configure a trunk without media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e2997-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e2997-104">

<span> </span></span></span>

<span data-ttu-id="e2997-105">_**Tópico da última modificação:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="e2997-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="e2997-106">Se quiser configurar um tronco com desvio de mídia desabilitado, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="e2997-106">If you want to configure a trunk with media bypass disabled, follow these steps.</span></span> <span data-ttu-id="e2997-107">Se você quiser configurar um tronco com bypass de mídia habilitado, consulte [configurar um tronco com bypass de mídia no Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md).</span><span class="sxs-lookup"><span data-stu-id="e2997-107">If you want to configure a trunk with media bypass enabled, see [Configure a trunk with media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md).</span></span>

<span data-ttu-id="e2997-p102">Uma configuração de tronco, como descrito abaixo, agrupa um conjunto de parâmetros que são aplicados a troncos designados com essa configuração. Uma determinada configuração de tronco pode ter o escopo de forma global (a todos os troncos que não têm uma configuração de site ou pool mais específica), para um site ou para um pool. A configuração de tronco no nível do pool é usada para definir o escopo de uma configuração específica de um tronco individual.</span><span class="sxs-lookup"><span data-stu-id="e2997-p102">A trunk configuration, as described below, groups a set of parameters that are applied to trunks assigned this trunk configuration. A particular trunk configuration can be scoped globally (to all trunks that do not have more specific site or pool configuration), or to a site, or to a pool. The pool-level trunk configuration is used to scope a specific trunk configuration to a single trunk.</span></span>

<span id="BKMK_ConfigTrunkGenericSteps"></span>

<div>

## <a name="to-configure-a-trunk-without-media-bypass"></a><span data-ttu-id="e2997-111">Para configurar um tronco sem bypass de mídia</span><span class="sxs-lookup"><span data-stu-id="e2997-111">To configure a trunk without media bypass</span></span>

1.  <span data-ttu-id="e2997-112">Faça logon no computador como um membro do grupo RTCUniversalServerAdmins ou como um membro da função CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="e2997-112">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="e2997-113">Para obter detalhes, consulte [delegar permissões de configuração no Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="e2997-113">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="e2997-114">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e2997-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e2997-115">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e2997-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e2997-116">Na barra de navegação à esquerda, clique em **Roteamento de Voz** e depois, em **Configuração do Tronco**.</span><span class="sxs-lookup"><span data-stu-id="e2997-116">In the left navigation bar, click **Voice Routing**, and then click **Trunk Configuration**.</span></span>

4.  <span data-ttu-id="e2997-117">Na página **Configuração do Tronco**, use um dos métodos a seguir para configurar um tronco:</span><span class="sxs-lookup"><span data-stu-id="e2997-117">On the **Trunk Configuration** page, use one of the following methods to configure a trunk:</span></span>
    
      - <span data-ttu-id="e2997-118">Dê um duplo clique em um tronco existente (por exemplo, o tronco **Global**) para exibir a caixa de diálogo **Editar Configuração do Tronco**.</span><span class="sxs-lookup"><span data-stu-id="e2997-118">Double-click an existing trunk (for example, the **Global** trunk) to display the **Edit Trunk Configuration** dialog box.</span></span>
    
      - <span data-ttu-id="e2997-119">Clique em **Novo** e depois, selecione um escopo para a nova configuração de tronco:</span><span class="sxs-lookup"><span data-stu-id="e2997-119">Click **New**, and then select a scope for the new trunk configuration:</span></span>
        
          - <span data-ttu-id="e2997-120">**Tronco de site:** Escolha o site para esta configuração de tronco em **Selecione um site** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2997-120">**Site trunk:** Choose the site for this trunk configuration in **Select a Site** , and then click **OK**.</span></span> <span data-ttu-id="e2997-121">Observe que se uma configuração de tronco já tiver sido criada para um site, o site não aparecerá em **Selecionar um Site**.</span><span class="sxs-lookup"><span data-stu-id="e2997-121">Note that if a trunk configuration has already been created for a site, the site does not appear in **Select a Site**.</span></span> <span data-ttu-id="e2997-122">Essa configuração de tronco será aplicada a todos os troncos no site.</span><span class="sxs-lookup"><span data-stu-id="e2997-122">This trunk configuration will be applied to all trunks in the site.</span></span>
        
          - <span data-ttu-id="e2997-123">**Tronco de pool:** Escolha o nome do tronco ao qual esta configuração de tronco se aplica em **Selecione um serviço** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2997-123">**Pool trunk:** Choose the name of the trunk that this trunk configuration applies to in **Select a Service** and click **OK**.</span></span> <span data-ttu-id="e2997-124">Esse tronco pode ser o tronco raiz ou qualquer tronco adicional definido no construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="e2997-124">This trunk can be the root trunk, or any additional trunks defined in Topology Builder.</span></span> <span data-ttu-id="e2997-125">Observe que se uma configuração de tronco já tiver sido criada para um tronco específico, o tronco não aparecerá em **Selecionar um Serviço**.</span><span class="sxs-lookup"><span data-stu-id="e2997-125">Note that if a trunk configuration has already been created for a specific trunk, the trunk does not appear in **Select a Service**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e2997-126">Depois de selecionar o escopo da configuração de tronco, ele não poderá ser alterado.</span><span class="sxs-lookup"><span data-stu-id="e2997-126">After you select the scope of the trunk configuration, it cannot be changed.</span></span><BR><span data-ttu-id="e2997-127">O campo <STRONG>Nome</STRONG> é pré-preenchido com o nome do site ou serviço associado à configuração de tronco e não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="e2997-127">The <STRONG>Name</STRONG> field is prepopulated with the name of the trunk configuration’s associated site or service and cannot be changed.</span></span>

    
    </div>

5.  <span data-ttu-id="e2997-128">Selecione uma das seguintes opções de **Nível de suporte de criptografia**:</span><span class="sxs-lookup"><span data-stu-id="e2997-128">Select one of the following **Encryption support level** options:</span></span>
    
      - <span data-ttu-id="e2997-129">**Obrigatório:** A criptografia do SRTP (protocolo de transporte em tempo real seguro) deve ser usada para ajudar a proteger o tráfego entre o servidor de mediação e o gateway ou PBX (Private Branch Exchange).</span><span class="sxs-lookup"><span data-stu-id="e2997-129">**Required:** Secure real-time transport protocol (SRTP) encryption must be used to help protect traffic between the Mediation Server and the gateway or private branch exchange (PBX).</span></span>
    
      - <span data-ttu-id="e2997-130">**Opcional:** A criptografia SRTP será usada se o provedor de serviços ou o fabricante de equipamento oferecer suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="e2997-130">**Optional:** SRTP encryption will be used if the service provider or equipment manufacturer supports it.</span></span>
    
      - <span data-ttu-id="e2997-131">**Sem suporte:** A criptografia do SRTP não é compatível com o provedor de serviços ou com o fabricante do equipamento e, portanto, não será usada.</span><span class="sxs-lookup"><span data-stu-id="e2997-131">**Not Supported:** SRTP encryption is not supported by the service provider or equipment manufacturer and therefore will not be used.</span></span>

6.  <span data-ttu-id="e2997-132">Certifique-se de que a caixa de seleção **Habilitar bypass de mídia** esteja desmarcada.</span><span class="sxs-lookup"><span data-stu-id="e2997-132">Be sure that the **Enable media bypass** check box is cleared.</span></span>

7.  <span data-ttu-id="e2997-133">Marque a caixa de seleção **processamento de mídia centralizado** se houver um ponto de terminação de mídia conhecido (por exemplo, um gateway PSTN (rede telefônica pública comutada) onde o término da mídia tem o mesmo IP que o término da sinalização.</span><span class="sxs-lookup"><span data-stu-id="e2997-133">Select the **Centralized media processing** check box if there is a well-known media termination point (for example, a public switched telephone network (PSTN) gateway where the media termination has the same IP as the signaling termination).</span></span> <span data-ttu-id="e2997-134">Desmarque esta opção se o tronco não possuir um ponto de terminação de mídia conhecido.</span><span class="sxs-lookup"><span data-stu-id="e2997-134">Clear this check box if the trunk does not have a well-known media termination point.</span></span>

8.  <span data-ttu-id="e2997-135">Se o par de troncos der suporte para receber solicitações de referência SIP do servidor de mediação, marque a caixa de seleção **habilitar o envio para o gateway** .</span><span class="sxs-lookup"><span data-stu-id="e2997-135">If the trunk peer supports receiving SIP REFER requests from the Mediation Server, select the **Enable sending refer to the gateway** check box.</span></span>

9.  <span data-ttu-id="e2997-136">(Opcional) Para permitir roteamento entre troncos, associe e configure os registros de uso de PSTN a essa configuração de tronco.</span><span class="sxs-lookup"><span data-stu-id="e2997-136">(Optional) To enable inter-trunk routing, associate and configure PSTN usage records to this trunk configuration.</span></span> <span data-ttu-id="e2997-137">Os usos de PSTN associados a essa configuração de tronco serão aplicados a todas as chamadas de entrada por meio do tronco que não se originam de um ponto de extremidade do Lync.</span><span class="sxs-lookup"><span data-stu-id="e2997-137">The PSTN usages associated to this trunk configuration will be applied for all incoming calls through the trunk that is not originating from a Lync endpoint.</span></span> <span data-ttu-id="e2997-138">Para gerenciar os registros de uso de PSTN associados à configuração de tronco, use um dos métodos a seguir:</span><span class="sxs-lookup"><span data-stu-id="e2997-138">To manage PSTN usage records associated to a trunk configuration, use one of the following methods:</span></span>
    
      - <span data-ttu-id="e2997-139">Para selecionar um ou mais registros de uma lista de todos os registros de uso PSTN disponíveis na sua implantação do Enterprise Voice, clique em **selecionar**.</span><span class="sxs-lookup"><span data-stu-id="e2997-139">To select one or more records from a list of all PSTN usage records available in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="e2997-140">Realce os registros que você deseja associar a essa configuração de tronco e depois, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2997-140">Highlight the records you want to associate with this trunk configuration and then click **OK**.</span></span>
    
      - <span data-ttu-id="e2997-141">Para remover um registro de uso de PSTN desta configuração de tronco, selecione o registro e clique em **Remover**.</span><span class="sxs-lookup"><span data-stu-id="e2997-141">To remove a PSTN usage record from this trunk configuration, select the record and click **Remove**.</span></span>
    
      - <span data-ttu-id="e2997-142">Para definir um novo registro de uso PSTN e associá-lo a essa configuração de tronco, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e2997-142">To define a new PSTN usage record and associate it with this trunk configuration, do the following:</span></span>
        
        1.  <span data-ttu-id="e2997-143">Clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e2997-143">Click **New**.</span></span>
        
        2.  <span data-ttu-id="e2997-144">No campo **Nome**, especifique um nome descritivo que seja exclusivo para o registro.</span><span class="sxs-lookup"><span data-stu-id="e2997-144">In the **Name** field, specify a descriptive name for the record that is unique.</span></span>
            
            <div>
            

            > [!NOTE]  
            > <span data-ttu-id="e2997-p110">O nome do registro de uso de PSTN deve ser exclusivo dentro de implantação do Enterprise Voice. Após a gravação do registro, o campo <STRONG>Nome</STRONG> não pode ser editado.</span><span class="sxs-lookup"><span data-stu-id="e2997-p110">The PSTN usage record name must be unique within the Enterprise Voice deployment. After the record is saved, the <STRONG>Name</STRONG> field cannot be edited.</span></span>

            
            </div>
        
        3.  <span data-ttu-id="e2997-147">Use um dos métodos a seguir para associar e configurar rotas para este registro de uso do PSTN:</span><span class="sxs-lookup"><span data-stu-id="e2997-147">Use one of the following methods to associate and configure routes for this PSTN usage record:</span></span>
            
              - <span data-ttu-id="e2997-148">Para selecionar uma ou mais rotas da lista de todas as rotas disponíveis na sua implantação do Enterprise Voice, clique em **selecionar**.</span><span class="sxs-lookup"><span data-stu-id="e2997-148">To select one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="e2997-149">Destaque as rotas que você deseja associar a esse registro de uso do PSTN e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2997-149">Highlight the routes you want to associate with this PSTN usage record, and click **OK**.</span></span>
            
              - <span data-ttu-id="e2997-150">Para remover uma rota do registro de uso do PSTN, selecione a rota e clique em **Remover**.</span><span class="sxs-lookup"><span data-stu-id="e2997-150">To remove a route from the PSTN usage record, select the route, and click **Remove**.</span></span>
            
              - <span data-ttu-id="e2997-151">Para definir uma nova rota e associá-la ao registro de uso do PSTN, clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e2997-151">To define a new route and associate it to this PSTN usage record, click **New**.</span></span> <span data-ttu-id="e2997-152">Para obter detalhes, consulte [criar uma rota de voz no Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="e2997-152">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
            
              - <span data-ttu-id="e2997-153">Para editar uma rota que está associada a esse registro de uso do PSTN, selecione a rota e clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="e2997-153">To edit a route that is associated with this PSTN usage record, select the route, and click **Show details**.</span></span> <span data-ttu-id="e2997-154">Para obter detalhes, consulte [modificar uma rota de voz no Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="e2997-154">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
        
        4.  <span data-ttu-id="e2997-155">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2997-155">Click **OK**.</span></span>
    
      - <span data-ttu-id="e2997-156">Para editar um registro de uso de PSTN que já está associado a essa configuração de tronco, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e2997-156">To edit a PSTN usage record that is already associated with this trunk configuration, do the following:</span></span>
        
        1.  <span data-ttu-id="e2997-157">Selecione o registro de uso do PSTN que você deseja editar e clique em **Mostrar detalhes**.</span><span class="sxs-lookup"><span data-stu-id="e2997-157">Select the PSTN usage record you want to edit, and click **Show details**.</span></span>
        
        2.  <span data-ttu-id="e2997-158">Use um dos métodos a seguir para associar e configurar rotas para este registro de uso do PSTN:</span><span class="sxs-lookup"><span data-stu-id="e2997-158">Use one of the following methods to associate and configure routes for this PSTN usage record:</span></span>
            
              - <span data-ttu-id="e2997-159">Para selecionar uma ou mais rotas da lista de todas as rotas disponíveis na sua implantação do Enterprise Voice, clique em **selecionar**.</span><span class="sxs-lookup"><span data-stu-id="e2997-159">To select one or more routes from the list of all available routes in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="e2997-160">Destaque as rotas que você deseja associar a esse registro de uso do PSTN e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2997-160">Highlight the routes you want to associate with this PSTN usage record, and click **OK**.</span></span>
            
              - <span data-ttu-id="e2997-161">Para remover uma rota do registro de uso do PSTN, selecione a rota e clique em **Remover**.</span><span class="sxs-lookup"><span data-stu-id="e2997-161">To remove a route from the PSTN usage record, select the route, and click **Remove**.</span></span>
            
              - <span data-ttu-id="e2997-162">Para definir uma nova rota e associá-la ao registro de uso do PSTN, clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e2997-162">To define a new route and associate it to this PSTN usage record, click **New**.</span></span> <span data-ttu-id="e2997-163">Para obter detalhes, consulte [criar uma rota de voz no Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="e2997-163">For details, see [Create a voice route in Lync Server 2013](lync-server-2013-create-a-voice-route.md).</span></span>
            
              - <span data-ttu-id="e2997-164">Para editar uma rota que está associada a esse registro de uso do PSTN, selecione a rota e clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="e2997-164">To edit a route that is associated with this PSTN usage record, select the route, and click **Show details**.</span></span> <span data-ttu-id="e2997-165">Para obter detalhes, consulte [modificar uma rota de voz no Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span><span class="sxs-lookup"><span data-stu-id="e2997-165">For details, see [Modify a voice route in Lync Server 2013](lync-server-2013-modify-a-voice-route.md).</span></span>
        
        3.  <span data-ttu-id="e2997-166">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2997-166">Click **OK**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e2997-167">É importante associar registros de uso PSTN de acordo com o peer do servidor de mediação associado ao tronco que está sendo configurado.</span><span class="sxs-lookup"><span data-stu-id="e2997-167">It important to associate PSTN usage records according to the Mediation Server peer that is associated to the trunk being configured.</span></span> <span data-ttu-id="e2997-168">Se o peer do servidor de mediação for um gateway PSTN ou um controle de borda de sessão (SBC), é altamente recomendável que a configuração de troncos não esteja associada a um registro de uso PSTN que roteia para um destino PSTN ou qualquer outro sistema downstream conectado via Lync Server.</span><span class="sxs-lookup"><span data-stu-id="e2997-168">If the Mediation Server peer is a PSTN gateway or a Session Border Controller (SBC), it is strongly recommended that the trunk configuration is not associated to a PSTN usage record that routes to a PSTN destination or any other downstream systems connected via Lync Server.</span></span>

    
    </div>

10. <span data-ttu-id="e2997-p118">Organize os registros de uso do PSTN para obter o melhor desempenho. Para alterar a posição de um registro na lista, selecione o registro de uso e clique na seta para cima ou para baixo.</span><span class="sxs-lookup"><span data-stu-id="e2997-p118">Arrange the PSTN usage records for optimum performance. To change a record’s position in the list, select the PSTN usage record, and click the up or down arrows.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e2997-171">A ordem na qual PSTN registros de uso são listados na configuração de tronco é significativa.</span><span class="sxs-lookup"><span data-stu-id="e2997-171">The order in which PSTN usage records are listed in the trunk configuration is significant.</span></span> <span data-ttu-id="e2997-172">O Lync Server percorre a lista de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="e2997-172">Lync Server traverses the list from top to down.</span></span>

    
    </div>

11. <span data-ttu-id="e2997-173">**Habilitar engatador RTP** deve ser selecionado para habilitar bypass de mídia para clientes sob um NAT ou firewall e um SBC que dê suporte ao engatador.</span><span class="sxs-lookup"><span data-stu-id="e2997-173">**Enable RTP Latching** should be selected to enable bypass media for clients behind a NAT or firewall and an SBC that supports latching.</span></span>

12. <span data-ttu-id="e2997-174">**Habilitar o histórico de chamadas de encaminhamento** deve ser selecionado para permitir o envio de informações de histórico de chamadas para o par de gateways do servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="e2997-174">**Enable forward call history** should be selected to enable sending of call history information to the gateway peer of the Mediation Server.</span></span>

13. <span data-ttu-id="e2997-175">**Habilitar encaminhar os dados de identidades P-declarados** devem ser selecionados para permitir que as informações do originador da chamada do pai sejam encaminhadas entre o servidor de mediação e o lado do gateway (e vice-versa), quando estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="e2997-175">**Enable forward P-Asserted-Identity data** should be selected to enable PAI call originator information to be forwarded between the Mediation Server side and gateway side (and vice versa), when present.</span></span>

14. <span data-ttu-id="e2997-176">**Enable outbound routing failover timer** deve ser selecionado para permitir failover rápido.</span><span class="sxs-lookup"><span data-stu-id="e2997-176">**Enable outbound routing failover timer** should be selected to enable fast failover.</span></span> <span data-ttu-id="e2997-177">O gateway associado a esse tronco pode fornecer notificações em 10 segundos de que está processando uma chamada de saída.</span><span class="sxs-lookup"><span data-stu-id="e2997-177">The gateway associated with this trunk can give notification within 10 seconds that it is processing an outbound call.</span></span> <span data-ttu-id="e2997-178">O redirecionamento para outro tronco ocorrerá se essa notificação não for recebida pelo servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="e2997-178">Rerouting to another trunk will occur if this notification is not received by the Mediation Server.</span></span> <span data-ttu-id="e2997-179">Em redes onde a latência pode atrasar o tempo de resposta ou o gateway levar mais de 10 segundos para responder, o failover rápido deverá ser desativado.</span><span class="sxs-lookup"><span data-stu-id="e2997-179">On networks where latency may delay the response time or the gateway takes longer than 10 seconds to respond, the fast failover should be disabled.</span></span>

15. <span data-ttu-id="e2997-180">(Opcional) Associe e configure as **regras de conversão do número de chamada** do tronco.</span><span class="sxs-lookup"><span data-stu-id="e2997-180">(Optional) Associate and configure **calling number translation rules** for the trunk.</span></span> <span data-ttu-id="e2997-181">Essas regras de conversão se aplicam ao número chamado para chamadas de saída.</span><span class="sxs-lookup"><span data-stu-id="e2997-181">These translation rules apply to the calling number for outbound calls</span></span>
    
      - <span data-ttu-id="e2997-182">Para escolher uma ou mais regras de uma lista de todas as regras de tradução que estão disponíveis na sua implantação do Enterprise Voice, clique em **selecionar**.</span><span class="sxs-lookup"><span data-stu-id="e2997-182">To choose one or more rules from a list of all translation rules that are available in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="e2997-183">Em **Selecionar Regras de Conversão**, clique nas regras que você deseja associar com o tronco, e depois em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2997-183">In **Select Translation Rules**, click the rules that you want to associate with the trunk, and then click **OK**.</span></span>
    
      - <span data-ttu-id="e2997-184">Para definir uma nova regra de conversão e associá-la ao tronco, clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e2997-184">To define a new translation rule and associate it with the trunk, click **New**.</span></span> <span data-ttu-id="e2997-185">Para obter detalhes sobre como definir uma nova regra, consulte [definindo regras de tradução no Lync Server 2013](lync-server-2013-defining-translation-rules.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="e2997-185">For details about defining a new rule, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="e2997-186">Para editar uma regra de conversão que já esteja associada ao tronco, clique no nome da regra e clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="e2997-186">To edit a translation rule that is already associated with the trunk, click the rule name, and then click **Show details**.</span></span> <span data-ttu-id="e2997-187">Para obter detalhes, consulte [definindo regras de tradução no Lync Server 2013](lync-server-2013-defining-translation-rules.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="e2997-187">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="e2997-188">Para copiar uma regra de conversão existente para usar como ponto de partida para definir uma nova regra, clique no nome da regra e clique em **Copiar** e clique em **Copiar**.</span><span class="sxs-lookup"><span data-stu-id="e2997-188">To copy an existing translation rule to use as a starting point for defining a new rule, click the rule name and click **Copy**, and then click **Paste**.</span></span> <span data-ttu-id="e2997-189">Para obter detalhes, consulte [definindo regras de tradução no Lync Server 2013](lync-server-2013-defining-translation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="e2997-189">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md).</span></span>
    
      - <span data-ttu-id="e2997-190">Para remover uma regra de conversão do tronco, destaque o nome da regra e clique em **Remover**.</span><span class="sxs-lookup"><span data-stu-id="e2997-190">To remove a translation rule from the trunk, highlight the rule name and click **Remove**.</span></span>
    
    <div>
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg398321.security(OCS.15).gif" title="segurança" alt="security" /><span data-ttu-id="e2997-192">Observação de segurança:</span><span class="sxs-lookup"><span data-stu-id="e2997-192">Security Note:</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="e2997-193">Não associe regras de conversão a um tronco se não houver regras de conversão configuradas no ponto do tronco associado porque as duas regras podem entrar em conflito.</span><span class="sxs-lookup"><span data-stu-id="e2997-193">Do not associate translation rules with a trunk if you have configured translation rules on the associated trunk peer, because the two rules might conflict.</span></span></td>
    </tr>
    </tbody>
    </table>
    
    </div>

16. <span data-ttu-id="e2997-p126">(Opcional) Associe e configure as **regras de conversão de números chamados** do tronco. As regras de conversão se aplicam ao número chamado em uma chamada de saída.</span><span class="sxs-lookup"><span data-stu-id="e2997-p126">(Optional) Associate and configure **called number translation rules** for the trunk. The translation rules apply to the called number in an outbound call.</span></span>
    
      - <span data-ttu-id="e2997-196">Para escolher uma ou mais regras de uma lista de todas as regras de tradução que estão disponíveis na sua implantação do Enterprise Voice, clique em **selecionar**.</span><span class="sxs-lookup"><span data-stu-id="e2997-196">To choose one or more rules from a list of all translation rules that are available in your Enterprise Voice deployment, click **Select**.</span></span> <span data-ttu-id="e2997-197">Em **Selecionar Regras de Conversão**, clique nas regras que você deseja associar com o tronco, e depois em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2997-197">In **Select Translation Rules**, click the rules that you want to associate with the trunk, and then click **OK**.</span></span>
    
      - <span data-ttu-id="e2997-198">Para definir uma nova regra de conversão e associá-la ao tronco, clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e2997-198">To define a new translation rule and associate it with the trunk, click **New**.</span></span> <span data-ttu-id="e2997-199">Para obter detalhes sobre como definir uma nova regra, consulte [definindo regras de tradução no Lync Server 2013](lync-server-2013-defining-translation-rules.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="e2997-199">For details about defining a new rule, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="e2997-200">Para editar uma regra de conversão que já esteja associada ao tronco, clique no nome da regra e clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="e2997-200">To edit a translation rule that is already associated with the trunk, click the rule name, and then click **Show details**.</span></span> <span data-ttu-id="e2997-201">Para obter detalhes, consulte [definindo regras de tradução no Lync Server 2013](lync-server-2013-defining-translation-rules.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="e2997-201">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="e2997-202">Para copiar uma regra de conversão existente para usar como ponto de partida para definir uma nova regra, clique no nome da regra e clique em **Copiar** e clique em **Copiar**.</span><span class="sxs-lookup"><span data-stu-id="e2997-202">To copy an existing translation rule to use as a starting point for defining a new rule, click the rule name and click **Copy**, and then click **Paste**.</span></span> <span data-ttu-id="e2997-203">Para obter detalhes, consulte [definindo regras de tradução no Lync Server 2013](lync-server-2013-defining-translation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="e2997-203">For details, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md).</span></span>
    
      - <span data-ttu-id="e2997-204">Para remover uma regra de conversão do tronco, destaque o nome da regra e clique em **Remover**.</span><span class="sxs-lookup"><span data-stu-id="e2997-204">To remove a translation rule from the trunk, highlight the rule name and click **Remove**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="e2997-205">Não associe regras de conversão a um tronco se não houver regras de conversão configuradas no ponto do tronco associado porque as duas regras podem entrar em conflito.</span><span class="sxs-lookup"><span data-stu-id="e2997-205">Do not associate translation rules with a trunk if you have configured translation rules on the associated trunk peer, because the two rules might conflict.</span></span>

    
    </div>

17. <span data-ttu-id="e2997-206">Verifique se as regras de conversão do tronco estão organizadas na ordem correta.</span><span class="sxs-lookup"><span data-stu-id="e2997-206">Make sure that the trunk’s translation rules are arranged in the correct order.</span></span> <span data-ttu-id="e2997-207">Para alterar a posição de uma regra na lista, realce o nome da regra e clique na seta para cima ou para baixo.</span><span class="sxs-lookup"><span data-stu-id="e2997-207">To change a rule’s position in the list, highlight the rule name, and then click the up or down arrow.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e2997-208">O Lync Server percorre a lista de regras de tradução de cima para baixo e usa a primeira regra que corresponde ao número discado.</span><span class="sxs-lookup"><span data-stu-id="e2997-208">Lync Server traverses the translation rule list from the top down and uses the first rule that matches the dialed number.</span></span> <span data-ttu-id="e2997-209">Se você configurar um tronco de forma que um número discado possa corresponder a mais de uma regra de conversão, certifique-se de que as regras mais restritivas estejam classificadas acima das regras menos restritivas.</span><span class="sxs-lookup"><span data-stu-id="e2997-209">If you configure a trunk so that a dialed number can match more than one translation rule, be sure that the more restrictive rules are sorted above the less restrictive rules.</span></span> <span data-ttu-id="e2997-210">Por exemplo, se você incluiu uma regra de conversão que corresponda a qualquer número de 11 dígitos e uma regra de conversão que corresponda somente a números de 11 dígitos que comecem com +1425, certifique-se de que a regra que corresponda a qualquer número de 11 dígitos esteja classificada <EM>abaixo</EM> da regra mais restritiva.</span><span class="sxs-lookup"><span data-stu-id="e2997-210">For example, if you have included a translation rule that matches any 11-digit number and a translation rule that matches only 11-digit numbers that start with +1425, be sure that the rule that matches any 11-digit number is sorted <EM>below</EM> the more restrictive rule.</span></span>

    
    </div>

18. <span data-ttu-id="e2997-211">Ao terminar de configurar o tronco, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2997-211">When you are finished configuring the trunk, click **OK**.</span></span>

19. <span data-ttu-id="e2997-212">Na página **Configuração do Tronco**, clique em **Confirmar** e clique em **Confirmar tudo**.</span><span class="sxs-lookup"><span data-stu-id="e2997-212">On the **Trunk Configuration** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e2997-213">Sempre que criar ou modificar uma configuração de tronco, você deve executar o comando <STRONG>Confirmar tudo</STRONG> para publicar a alteração na configuração.</span><span class="sxs-lookup"><span data-stu-id="e2997-213">Whenever you create or modify a trunk configuration, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="e2997-214">Para obter detalhes, consulte <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">publicar alterações pendentes na configuração de roteamento de voz no Lync Server 2013</A> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="e2997-214">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e2997-215">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2997-215">See Also</span></span>


[<span data-ttu-id="e2997-216">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2997-216">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)  


[<span data-ttu-id="e2997-217">Definindo regras de tradução no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e2997-217">Defining translation rules in Lync Server 2013</span></span>](lync-server-2013-defining-translation-rules.md)  
  

<span data-ttu-id="e2997-218"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e2997-218"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

