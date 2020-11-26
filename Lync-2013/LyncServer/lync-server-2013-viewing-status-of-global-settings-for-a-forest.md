---
title: 'Lync Server 2013: exibindo o status de configurações globais para uma floresta'
description: 'Lync Server 2013: exibindo o status de configurações globais para uma floresta.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View status of global settings for a forest
ms:assetid: 2ab0f2f1-9908-4e6f-aff3-d6b3cc474b6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747889(v=OCS.15)
ms:contentKeyID: 63969590
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9f722ea66f6c54c816703bd1af1d3def57bbd84
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443906"
---
# <a name="view-status-of-global-settings-for-a-forest-in-lync-server-2013"></a><span data-ttu-id="295e2-103">Exibir o status das configurações globais de uma floresta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="295e2-103">View status of global settings for a forest in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="295e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="295e2-104">

<span> </span></span></span>

<span data-ttu-id="295e2-105">_**Tópico da última modificação:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="295e2-105">_**Topic Last Modified:** 2014-05-20_</span></span>

<span data-ttu-id="295e2-106">Os administradores devem analisar as configurações globais para uma implantação do Lync Server 2013 mensalmente.</span><span class="sxs-lookup"><span data-stu-id="295e2-106">Administrators should review the global settings for a Lync Server 2013 deployment monthly.</span></span> <span data-ttu-id="295e2-107">O objetivo seria revisar as configurações implementadas em relação a um conjunto de configurações conhecidas, uma configuração de linha de base para ajudar a garantir que as configurações sejam válidas e determinar se a documentação da linha de base deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="295e2-107">The objective would be to review implemented settings against a set of known configurations—a baseline configuration to help guarantee that settings are valid and to determine whether the baseline documentation should be updated.</span></span> <span data-ttu-id="295e2-108">As alterações na configuração global devem ser implementadas por meio de um processo de controle de alterações que deve incluir a documentação das novas configurações.</span><span class="sxs-lookup"><span data-stu-id="295e2-108">Changes to global setting should be implemented through a Change Control process which should include documenting the new settings.</span></span>

<span data-ttu-id="295e2-109">As configurações globais que devem ser analisadas estão descritas nas seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="295e2-109">Global settings that should be reviewed are described in the following sections:</span></span>

<div>

## <a name="check-general-settings"></a><span data-ttu-id="295e2-110">Verificar as configurações gerais</span><span class="sxs-lookup"><span data-stu-id="295e2-110">Check general settings</span></span>

<span data-ttu-id="295e2-111">Verifique as configurações gerais, incluindo os domínios SIP (Session Initiation Protocol) com suporte para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="295e2-111">Check general settings, including the supported Session Initiation Protocol (SIP) domains for Lync Server 2013.</span></span>

<span data-ttu-id="295e2-112">As informações do domínio SIP podem ser retornadas usando o Windows PowerShell e o cmdlet **Get-CsSipDomain** .</span><span class="sxs-lookup"><span data-stu-id="295e2-112">SIP domain information can be returned by using Windows PowerShell and the **Get-CsSipDomain** cmdlet.</span></span> <span data-ttu-id="295e2-113">Para retornar essas informações, execute o `Get-CsSipDomain` comando do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="295e2-113">To return this information, run the `Get-CsSipDomain` Windows PowerShell command.</span></span>

<span data-ttu-id="295e2-114">Get-CsSipDomain retornará informações semelhantes para todos os domínios SIP autorizados:</span><span class="sxs-lookup"><span data-stu-id="295e2-114">Get-CsSipDomain will return information similar to this for all the authorized SIP domains:</span></span>

<span data-ttu-id="295e2-115">Nome da identidade-padrão</span><span class="sxs-lookup"><span data-stu-id="295e2-115">Identity Name IsDefault</span></span>

<span data-ttu-id="295e2-116">\-------- ---- ---------</span><span class="sxs-lookup"><span data-stu-id="295e2-116">\-------- ---- ---------</span></span>

<span data-ttu-id="295e2-117">fabrikam.com fabrikam.com verdadeiro</span><span class="sxs-lookup"><span data-stu-id="295e2-117">fabrikam.com fabrikam.com True</span></span>

<span data-ttu-id="295e2-118">na.fabrikam.com na.fabrikam.com falso</span><span class="sxs-lookup"><span data-stu-id="295e2-118">na.fabrikam.com na.fabrikam.com False</span></span>

<span data-ttu-id="295e2-119">Se a Propriedade IsDefault estiver definida como true, o domínio correspondente será o seu domínio SIP padrão.</span><span class="sxs-lookup"><span data-stu-id="295e2-119">If the IsDefault property is set to True, the corresponding domain is your default SIP domain.</span></span> <span data-ttu-id="295e2-120">Você pode usar o cmdlet Set-CsSipDomain para alterar o domínio SIP padrão de sua organização.</span><span class="sxs-lookup"><span data-stu-id="295e2-120">You can use the Set-CsSipDomain cmdlet to change the default SIP domain for your organization.</span></span> <span data-ttu-id="295e2-121">No entanto, você não pode apenas excluir o domínio SIP padrão porque isso o deixaria sem um domínio padrão.</span><span class="sxs-lookup"><span data-stu-id="295e2-121">However, you can't just delete the default SIP domain because that would leave you without a default domain.</span></span> <span data-ttu-id="295e2-122">Se você quisesse excluir o domínio fabrikam.com (conforme mostrado no exemplo anterior), primeiro precisaria configurar na.fabrikam.com para ser o domínio padrão.</span><span class="sxs-lookup"><span data-stu-id="295e2-122">If you wanted to delete the fabrikam.com domain (as shown in the previous example), you would first have to configure na.fabrikam.com to be your default domain.</span></span>

</div>

<div>

## <a name="check-meeting-settings"></a><span data-ttu-id="295e2-123">Verificar as configurações da reunião</span><span class="sxs-lookup"><span data-stu-id="295e2-123">Check meeting settings</span></span>

<span data-ttu-id="295e2-124">As configurações de reunião incluem definições de política de reunião e suporte para a participação de usuários anônimos em reuniões.</span><span class="sxs-lookup"><span data-stu-id="295e2-124">Meeting settings include meeting policy definitions and support for participation of anonymous users in meetings.</span></span>

<span data-ttu-id="295e2-125">As definições de configuração de reunião podem ser recuperadas usando o Windows PowerShell e o cmdlet **Get-CsMeetingConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="295e2-125">Meeting configuration settings can be retrieved by using Windows PowerShell and the **Get-CsMeetingConfiguration** cmdlet.</span></span> <span data-ttu-id="295e2-126">Por exemplo, esse comando retorna informações sobre as definições de configuração de reunião global:</span><span class="sxs-lookup"><span data-stu-id="295e2-126">For example, this command returns information about the global meeting configuration settings:</span></span>

<span data-ttu-id="295e2-127">Get-CsMeetingConfiguration – as configurações de reunião "global" de identidade também podem ser configuradas no escopo do site.</span><span class="sxs-lookup"><span data-stu-id="295e2-127">Get-CsMeetingConfiguration –Identity "Global"Meeting configuration settings can also be configured at the site scope.</span></span> <span data-ttu-id="295e2-128">Por isso, talvez você queira usar o seguinte comando, que retorna informações sobre todas as definições de configuração de reunião:</span><span class="sxs-lookup"><span data-stu-id="295e2-128">Because of that, you might want to use the following command, which returns information about all the meeting configuration settings:</span></span>

`Get-CsMeetingConfiguration`

<span data-ttu-id="295e2-129">O cmdlet **Get-CsMeetingConfiguration** retorna informações semelhantes às seguintes:</span><span class="sxs-lookup"><span data-stu-id="295e2-129">The **Get-CsMeetingConfiguration** cmdlet returns information similar to the following:</span></span>

<span data-ttu-id="295e2-130">Identidade: global</span><span class="sxs-lookup"><span data-stu-id="295e2-130">Identity : Global</span></span>

<span data-ttu-id="295e2-131">PstnCallersBypassLobby: true</span><span class="sxs-lookup"><span data-stu-id="295e2-131">PstnCallersBypassLobby : True</span></span>

<span data-ttu-id="295e2-132">EnableAssignedConferenceType: true</span><span class="sxs-lookup"><span data-stu-id="295e2-132">EnableAssignedConferenceType : True</span></span>

<span data-ttu-id="295e2-133">DesignateAsPresenter: empresa</span><span class="sxs-lookup"><span data-stu-id="295e2-133">DesignateAsPresenter : Company</span></span>

<span data-ttu-id="295e2-134">AssignedConferenceTypeByDefault: true</span><span class="sxs-lookup"><span data-stu-id="295e2-134">AssignedConferenceTypeByDefault : True</span></span>

<span data-ttu-id="295e2-135">AdmitAnonymousUsersByDefault: true</span><span class="sxs-lookup"><span data-stu-id="295e2-135">AdmitAnonymousUsersByDefault : True</span></span>

<span data-ttu-id="295e2-136">Novamente, o item final na lista, **AdmitAnonymousUsersByDefault**, habilita ou desabilita a capacidade dos usuários anônimos de participarem de reuniões.</span><span class="sxs-lookup"><span data-stu-id="295e2-136">Again, the final item in the list, **AdmitAnonymousUsersByDefault**, enables or disables the ability of anonymous users to participate in meetings.</span></span>

<span data-ttu-id="295e2-137">Ao verificar as configurações de reunião, talvez seja útil comparar as configurações atuais com relação aos equivalentes padrão.</span><span class="sxs-lookup"><span data-stu-id="295e2-137">When checking meeting configuration settings, you might find it useful to compare the current settings against the default equivalents.</span></span> <span data-ttu-id="295e2-138">Você pode visualizar as configurações de reunião padrão executando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="295e2-138">You can view the default meeting configuration settings by running the following command:</span></span>

`New-CsMeetingConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="295e2-139">O comando anterior cria uma instância de configuração de reunião global somente na memória, uma instância que usa o valor padrão para cada propriedade.</span><span class="sxs-lookup"><span data-stu-id="295e2-139">The previous command creates an in-memory-only instance of the global meeting configuration settings, an instance that uses the default value for each property.</span></span> <span data-ttu-id="295e2-140">Nenhuma configuração de reunião real é criada quando você executa o comando.</span><span class="sxs-lookup"><span data-stu-id="295e2-140">No actual meeting configuration settings are created when you run the command.</span></span> <span data-ttu-id="295e2-141">No entanto, todos os valores de propriedades padrão serão exibidos na tela.</span><span class="sxs-lookup"><span data-stu-id="295e2-141">However, all the default property values will be displayed on-screen.</span></span>

</div>

<div>

## <a name="check-edge-servers-and-their-settings"></a><span data-ttu-id="295e2-142">Verificar os servidores de borda e suas configurações</span><span class="sxs-lookup"><span data-stu-id="295e2-142">Check Edge Servers and their settings</span></span>

<span data-ttu-id="295e2-143">As informações do servidor de borda podem ser recuperadas usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="295e2-143">Edge Server information can be retrieved by using Windows PowerShell.</span></span> <span data-ttu-id="295e2-144">Esse comando retorna informações sobre todos os servidores de borda configurados para uso em sua organização:</span><span class="sxs-lookup"><span data-stu-id="295e2-144">This command returns information about all the Edge Servers configured for use in your organization:</span></span>

`Get-CsService -EdgeServer`

<span data-ttu-id="295e2-145">As informações retornadas incluem todas as configurações de FQDN e de porta para cada servidor de borda:</span><span class="sxs-lookup"><span data-stu-id="295e2-145">The returned information includes all of the FQDN and port settings for each Edge Server:</span></span>

<span data-ttu-id="295e2-146">Identidade: EdgeServer: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="295e2-146">Identity : EdgeServer: dc.fabrikam.com</span></span>

<span data-ttu-id="295e2-147">Registrador: registrar: LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="295e2-147">Registrar : Registrar: LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="295e2-148">AccessEdgeInternalSipPort: 5061</span><span class="sxs-lookup"><span data-stu-id="295e2-148">AccessEdgeInternalSipPort : 5061</span></span>

<span data-ttu-id="295e2-149">AccessEdgeExternalSipPort: 5061</span><span class="sxs-lookup"><span data-stu-id="295e2-149">AccessEdgeExternalSipPort : 5061</span></span>

<span data-ttu-id="295e2-150">AccessEdgeClientPort: 443</span><span class="sxs-lookup"><span data-stu-id="295e2-150">AccessEdgeClientPort : 443</span></span>

<span data-ttu-id="295e2-151">DataPsomServerPort: 8057</span><span class="sxs-lookup"><span data-stu-id="295e2-151">DataPsomServerPort : 8057</span></span>

<span data-ttu-id="295e2-152">DataPsomClientPort: 444</span><span class="sxs-lookup"><span data-stu-id="295e2-152">DataPsomClientPort : 444</span></span>

<span data-ttu-id="295e2-153">MediaRelayAuthEdgePort: 5062</span><span class="sxs-lookup"><span data-stu-id="295e2-153">MediaRelayAuthEdgePort : 5062</span></span>

<span data-ttu-id="295e2-154">MediaRelayAuthInternalTurnTcpPort: 443</span><span class="sxs-lookup"><span data-stu-id="295e2-154">MediaRelayAuthInternalTurnTcpPort : 443</span></span>

<span data-ttu-id="295e2-155">MediaRelayAuthExternalTurnTcpPort: 445</span><span class="sxs-lookup"><span data-stu-id="295e2-155">MediaRelayAuthExternalTurnTcpPort : 445</span></span>

<span data-ttu-id="295e2-156">MediaRelayAuthInternalTurnUdpPort: 3478</span><span class="sxs-lookup"><span data-stu-id="295e2-156">MediaRelayAuthInternalTurnUdpPort : 3478</span></span>

<span data-ttu-id="295e2-157">MediaRelayAuthExternalTurnUdpPort: 3478</span><span class="sxs-lookup"><span data-stu-id="295e2-157">MediaRelayAuthExternalTurnUdpPort : 3478</span></span>

<span data-ttu-id="295e2-158">MediaCommunicationPortStart: 50000</span><span class="sxs-lookup"><span data-stu-id="295e2-158">MediaCommunicationPortStart : 50000</span></span>

<span data-ttu-id="295e2-159">MediaComunicationPortCount: 10000</span><span class="sxs-lookup"><span data-stu-id="295e2-159">MediaComunicationPortCount : 10000</span></span>

<span data-ttu-id="295e2-160">AccessEdgeExternalFqdn: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="295e2-160">AccessEdgeExternalFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="295e2-161">DataEdgeExternalFqdn: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="295e2-161">DataEdgeExternalFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="295e2-162">AVEdgeExternalFqdn :</span><span class="sxs-lookup"><span data-stu-id="295e2-162">AVEdgeExternalFqdn :</span></span>

<span data-ttu-id="295e2-163">InternalInterfaceFqdn :</span><span class="sxs-lookup"><span data-stu-id="295e2-163">InternalInterfaceFqdn :</span></span>

<span data-ttu-id="295e2-164">ExternalMrasFqdn: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="295e2-164">ExternalMrasFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="295e2-165">DependentServiceList: {registrador: LYNC-SE.fabrikam.com,</span><span class="sxs-lookup"><span data-stu-id="295e2-165">DependentServiceList : {Registrar:LYNC-SE.fabrikam.com,</span></span>

<span data-ttu-id="295e2-166">ConferencingServer: LYNC-SE. fabrikam</span><span class="sxs-lookup"><span data-stu-id="295e2-166">ConferencingServer:LYNC-SE.fabrikam</span></span>

<span data-ttu-id="295e2-167">com, MediationServer: LYNC-SE.</span><span class="sxs-lookup"><span data-stu-id="295e2-167">com, MediationServer:LYNC-SE.</span></span>

<span data-ttu-id="295e2-168">fabrikam.com}</span><span class="sxs-lookup"><span data-stu-id="295e2-168">fabrikam.com}</span></span>

<span data-ttu-id="295e2-169">ServiceId: fabrikam.com-EdgeServer-2</span><span class="sxs-lookup"><span data-stu-id="295e2-169">ServiceId : fabrikam.com-EdgeServer-2</span></span>

<span data-ttu-id="295e2-170">SiteId: site:fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="295e2-170">SiteId : site:fabrikam.com</span></span>

<span data-ttu-id="295e2-171">PoolFqdn: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="295e2-171">PoolFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="295e2-172">Versão: 5</span><span class="sxs-lookup"><span data-stu-id="295e2-172">Version : 5</span></span>

<span data-ttu-id="295e2-173">Função: EdgeServer</span><span class="sxs-lookup"><span data-stu-id="295e2-173">Role : EdgeServer</span></span>

<div>

## <a name="check-federation-settings"></a><span data-ttu-id="295e2-174">Verificar as configurações de Federação</span><span class="sxs-lookup"><span data-stu-id="295e2-174">Check federation settings</span></span>

<span data-ttu-id="295e2-175">Verifique as configurações de Federação, como se ela está configurada e, se a resposta for "Sim", o FQDN e a porta.</span><span class="sxs-lookup"><span data-stu-id="295e2-175">Check Federation settings, such as whether it is configured and, if the answer is "yes,", the FQDN and port.</span></span> <span data-ttu-id="295e2-176">A Federação está habilitada e desabilitada usando a coleção global de definições de configuração de borda de acesso.</span><span class="sxs-lookup"><span data-stu-id="295e2-176">Federation is enabled and disabled by using the global collection of Access Edge configuration settings.</span></span> <span data-ttu-id="295e2-177">Entre outras coisas, isso significa que a Federação está configurada com base em tudo ou nada: a Federação está habilitada para toda a organização ou a Federação está desabilitada para toda a organização</span><span class="sxs-lookup"><span data-stu-id="295e2-177">Among other things, these mean that federation is configured on an all-or-nothing basis: either federation is enabled for the whole organization or federation is disabled for the whole organization</span></span>

<span data-ttu-id="295e2-178">Suas configurações de borda de acesso podem ser retornadas usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="295e2-178">Your Access Edge configuration settings can be returned by using Windows PowerShell.</span></span> <span data-ttu-id="295e2-179">Para fazer isso, execute o seguinte comando do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="295e2-179">To do that, run the following Windows PowerShell command:</span></span>

`Get-CsAccessEdgeConfiguration`

<span data-ttu-id="295e2-180">Por sua vez, esse comando retornará dados semelhantes a isto:</span><span class="sxs-lookup"><span data-stu-id="295e2-180">In turn, that command will return data similar to this:</span></span>

<span data-ttu-id="295e2-181">Identidade: global</span><span class="sxs-lookup"><span data-stu-id="295e2-181">Identity : Global</span></span>

<span data-ttu-id="295e2-182">AllowAnonymousUsers: false</span><span class="sxs-lookup"><span data-stu-id="295e2-182">AllowAnonymousUsers : False</span></span>

<span data-ttu-id="295e2-183">AllowFederatedUsers: false</span><span class="sxs-lookup"><span data-stu-id="295e2-183">AllowFederatedUsers : False</span></span>

<span data-ttu-id="295e2-184">AllowOutsideUsers: false</span><span class="sxs-lookup"><span data-stu-id="295e2-184">AllowOutsideUsers : False</span></span>

<span data-ttu-id="295e2-185">Myclearinghouse: falso</span><span class="sxs-lookup"><span data-stu-id="295e2-185">BeClearingHouse : False</span></span>

<span data-ttu-id="295e2-186">EnablePartnerDiscovery: false</span><span class="sxs-lookup"><span data-stu-id="295e2-186">EnablePartnerDiscovery : False</span></span>

<span data-ttu-id="295e2-187">EnableArchivingDisclaimer: false</span><span class="sxs-lookup"><span data-stu-id="295e2-187">EnableArchivingDisclaimer : False</span></span>

<span data-ttu-id="295e2-188">KeepCrlsUpToDateForPeers: true</span><span class="sxs-lookup"><span data-stu-id="295e2-188">KeepCrlsUpToDateForPeers : True</span></span>

<span data-ttu-id="295e2-189">MarkSourceVerifiableOnOutgoingMessages: true</span><span class="sxs-lookup"><span data-stu-id="295e2-189">MarkSourceVerifiableOnOutgoingMessages : True</span></span>

<span data-ttu-id="295e2-190">OutgoingTlsCountForFederatedPartners: 4</span><span class="sxs-lookup"><span data-stu-id="295e2-190">OutgoingTlsCountForFederatedPartners : 4</span></span>

<span data-ttu-id="295e2-191">RoutingMethod : UseDnsSrvRouting</span><span class="sxs-lookup"><span data-stu-id="295e2-191">RoutingMethod : UseDnsSrvRouting</span></span>

<span data-ttu-id="295e2-192">Se a propriedade **AllowFederatedUsers** estiver definida como true, isso significa que a Federação está habilitada para sua organização.</span><span class="sxs-lookup"><span data-stu-id="295e2-192">If the **AllowFederatedUsers** property is set to True, that means that federation is enabled for your organization.</span></span> <span data-ttu-id="295e2-193">(Definir **AllowFederatedUsers** como true também significa que, em um cenário de domínio dividido, os usuários locais poderão se comunicar perfeitamente com seus usuários na nuvem.)</span><span class="sxs-lookup"><span data-stu-id="295e2-193">(Setting **AllowFederatedUsers** to True also means that, in a split domain scenario, your on-premises users will be able to communicate seamlessly with your in-the-cloud users.)</span></span>

<span data-ttu-id="295e2-194">Para recuperar as configurações de FQDN e de porta do servidor de borda, consulte a tarefa anterior (servidores de borda e suas configurações).</span><span class="sxs-lookup"><span data-stu-id="295e2-194">To retrieve the FQDN and port settings for your Edge Server, see the previous task (Edge Servers and their settings).</span></span>

<span data-ttu-id="295e2-195">Habilitar a Federação no escopo global apenas significa que os usuários podem se comunicar com usuários federados.</span><span class="sxs-lookup"><span data-stu-id="295e2-195">Enabling federation at the global scope only means that users can potentially communicate with federated users.</span></span> <span data-ttu-id="295e2-196">Para determinar se os usuários individuais podem realmente se comunicar com usuários federados exigem que você examine a política de acesso de usuários externos atribuída a esse usuário.</span><span class="sxs-lookup"><span data-stu-id="295e2-196">To determine whether any individual users can actually communicate with federated users requires you to examine the external user access policy assigned to that user.</span></span>

<span data-ttu-id="295e2-197">As informações de acesso do usuário externo podem ser retornadas usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="295e2-197">External user access information can be returned by using Windows PowerShell.</span></span> <span data-ttu-id="295e2-198">Por exemplo, esse comando retorna informações para a política de acesso externo ao usuário externo:</span><span class="sxs-lookup"><span data-stu-id="295e2-198">For example, this command returns information for the global external user access policy:</span></span>

`Get-CsExternalAccessPolicy -Identity "Global"`

<span data-ttu-id="295e2-199">E esse comando retorna informações para todas as políticas de acesso externo do usuário:</span><span class="sxs-lookup"><span data-stu-id="295e2-199">And this command returns information for all the external user access policies:</span></span>

`Get-CsExternalAccessPolicy`

<span data-ttu-id="295e2-200">As informações retornadas serão parecidas com isto:</span><span class="sxs-lookup"><span data-stu-id="295e2-200">The returned information will resemble this:</span></span>

<span data-ttu-id="295e2-201">Identidade: falso</span><span class="sxs-lookup"><span data-stu-id="295e2-201">Identity : False</span></span>

<span data-ttu-id="295e2-202">Descritivo</span><span class="sxs-lookup"><span data-stu-id="295e2-202">Description :</span></span>

<span data-ttu-id="295e2-203">EnableFederationAccess: false</span><span class="sxs-lookup"><span data-stu-id="295e2-203">EnableFederationAccess : False</span></span>

<span data-ttu-id="295e2-204">EnablePublicCloudAccess: false</span><span class="sxs-lookup"><span data-stu-id="295e2-204">EnablePublicCloudAccess : False</span></span>

<span data-ttu-id="295e2-205">EnablePublicCloudAccessAudioVideoAccess: false</span><span class="sxs-lookup"><span data-stu-id="295e2-205">EnablePublicCloudAccessAudioVideoAccess : False</span></span>

<span data-ttu-id="295e2-206">EnableOutsideAccess: false</span><span class="sxs-lookup"><span data-stu-id="295e2-206">EnableOutsideAccess : False</span></span>

<span data-ttu-id="295e2-207">Se **EnableFederationAccess** for definido como true, os usuários gerenciados pela política fornecida poderão se comunicar com os usuários federados.</span><span class="sxs-lookup"><span data-stu-id="295e2-207">If **EnableFederationAccess** is set to True, then users managed by the given policy can communicate with federated users.</span></span>

</div>

</div>

<div>

## <a name="check-archiving-settings"></a><span data-ttu-id="295e2-208">Verificar as configurações de arquivamento</span><span class="sxs-lookup"><span data-stu-id="295e2-208">Check archiving settings</span></span>

<span data-ttu-id="295e2-209">Verifique as configurações de arquivamento para comunicações internas e federadas. Antes de verificar as configurações de arquivamento interno e externo, verifique se o arquivamento está habilitado.</span><span class="sxs-lookup"><span data-stu-id="295e2-209">Check archiving settings for internal and federated communications.Before verifying the settings for internal and external archiving, you should verify that archiving is enabled.</span></span>

<span data-ttu-id="295e2-210">As configurações de arquivamento podem ser verificadas usando o Windows PowerShell e o Get-CsArchivingConfiguration cmdlet:</span><span class="sxs-lookup"><span data-stu-id="295e2-210">Archiving configuration settings can be verified by using Windows PowerShell and the Get-CsArchivingConfiguration cmdlet:</span></span>

`Get-CsArchivingConfiguration -Identity "Global"`

<span data-ttu-id="295e2-211">Observe que as configurações de arquivamento também podem ser configuradas no escopo do site.</span><span class="sxs-lookup"><span data-stu-id="295e2-211">Note that archiving settings can also be configured at the site scope.</span></span> <span data-ttu-id="295e2-212">Para retornar informações sobre todas as configurações de arquivamento, use este comando:</span><span class="sxs-lookup"><span data-stu-id="295e2-212">To return information about all the archiving settings, use this command:</span></span>

`Get-CsArchivingConfiguration`

<span data-ttu-id="295e2-213">O cmdlet Get-CsArchivingConfiguration retorna dados semelhantes a este:</span><span class="sxs-lookup"><span data-stu-id="295e2-213">The Get-CsArchivingConfiguration cmdlet returns data similar to this:</span></span>

<span data-ttu-id="295e2-214">Identidade: global</span><span class="sxs-lookup"><span data-stu-id="295e2-214">Identity : Global</span></span>

<span data-ttu-id="295e2-215">EnableArchiving: false</span><span class="sxs-lookup"><span data-stu-id="295e2-215">EnableArchiving : False</span></span>

<span data-ttu-id="295e2-216">EnablePurging: false</span><span class="sxs-lookup"><span data-stu-id="295e2-216">EnablePurging : False</span></span>

<span data-ttu-id="295e2-217">PurgeExportedArchivesOnly: false</span><span class="sxs-lookup"><span data-stu-id="295e2-217">PurgeExportedArchivesOnly : False</span></span>

<span data-ttu-id="295e2-218">BlockOnArchiveFailure: false</span><span class="sxs-lookup"><span data-stu-id="295e2-218">BlockOnArchiveFailure : False</span></span>

<span data-ttu-id="295e2-219">KeepArchivingDataForDays: 14</span><span class="sxs-lookup"><span data-stu-id="295e2-219">KeepArchivingDataForDays : 14</span></span>

<span data-ttu-id="295e2-220">PurgeHourOfDay: 2</span><span class="sxs-lookup"><span data-stu-id="295e2-220">PurgeHourOfDay : 2</span></span>

<span data-ttu-id="295e2-221">ArchiveDuplicateMessages: true</span><span class="sxs-lookup"><span data-stu-id="295e2-221">ArchiveDuplicateMessages : True</span></span>

<span data-ttu-id="295e2-222">CachePurgingInterval: 24</span><span class="sxs-lookup"><span data-stu-id="295e2-222">CachePurgingInterval : 24</span></span>

<span data-ttu-id="295e2-223">Se a propriedade EnableArchiving estiver definida como false, isso significa que nenhuma sessão de comunicação será arquivada.</span><span class="sxs-lookup"><span data-stu-id="295e2-223">If the EnableArchiving property is set to False, that means that no communication sessions will be archived.</span></span> <span data-ttu-id="295e2-224">Se você quiser arquivar sessões de mensagens instantâneas somente, use um comando como o seguinte para habilitar o arquivamento de sessões de mensagens instantâneas:</span><span class="sxs-lookup"><span data-stu-id="295e2-224">If you want to archive instant messaging sessions only, use a command such as the following to enable the archiving of IM sessions:</span></span>

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

<span data-ttu-id="295e2-225">Para arquivar sessões de conferência e sessões de mensagens instantâneas, use este comando:</span><span class="sxs-lookup"><span data-stu-id="295e2-225">To archive conferencing sessions and instant messaging sessions, use this command:</span></span>

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

<span data-ttu-id="295e2-226">Se quiser comparar as configurações atuais de arquivamento com as configurações padrão, execute o seguinte comando do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="295e2-226">If you’d like to compare your current archiving settings with the default settings, run the following Windows PowerShell command:</span></span>

`New-CsArchivingConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="295e2-227">Esse comando cria uma instância somente na memória das configurações de configuração global de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="295e2-227">That command creates an in-memory-only instance of the global archiving configuration settings.</span></span> <span data-ttu-id="295e2-228">Este não é um conjunto real de configurações que é usado pelo Lync Server.</span><span class="sxs-lookup"><span data-stu-id="295e2-228">This is not a real collection of settings that is used by Lync Server.</span></span> <span data-ttu-id="295e2-229">No entanto, ele exibe os valores padrão para todas as propriedades de configuração de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="295e2-229">However, it does display the default values for all the archiving configuration properties.</span></span>

<span data-ttu-id="295e2-230">Você também pode usar esse comando para retornar o FQDN dos seus servidores de arquivamento:</span><span class="sxs-lookup"><span data-stu-id="295e2-230">You can also use this command to return the FQDN of your Archiving servers:</span></span>

`Get-CsService -ArchivingServer`

<span data-ttu-id="295e2-231">Depois de verificar se o arquivamento está habilitado, você pode ver as políticas de arquivamento para determinar se as sessões de comunicação internas e externas estão sendo arquivadas.</span><span class="sxs-lookup"><span data-stu-id="295e2-231">After you have verified that archiving is enabled, you can then view your archiving policies to determine whether internal and external communication sessions are being archived.</span></span>

<span data-ttu-id="295e2-232">As informações da política de arquivamento podem ser recuperadas usando o cmdlet Get-CsArchivingPolicy.</span><span class="sxs-lookup"><span data-stu-id="295e2-232">Archiving policy information can be retrieved by using the Get-CsArchivingPolicy cmdlet.</span></span> <span data-ttu-id="295e2-233">Por exemplo, esse comando retorna informações sobre a política de arquivamento global:</span><span class="sxs-lookup"><span data-stu-id="295e2-233">For example, this command returns information about the global archiving policy:</span></span>

`Get-CsArchivingPolicy -Identity "Global"`

<span data-ttu-id="295e2-234">Como as políticas de arquivamento também podem ser configuradas no site e no escopo por usuário, você também pode querer usar esse comando, que retorna informações sobre todas as políticas de arquivamento:</span><span class="sxs-lookup"><span data-stu-id="295e2-234">Because archiving policies can also be configured at the site and the per-user scope, you might also want to use this command, which returns information about all the archiving policies:</span></span>

`Get-CsArchivingPolicy`

<span data-ttu-id="295e2-235">As informações recebidas do Get-CsArchivingPolicy serão parecidas com isto:</span><span class="sxs-lookup"><span data-stu-id="295e2-235">The information that you receive from Get-CsArchivingPolicy will resemble this:</span></span>

<span data-ttu-id="295e2-236">Identidade: global</span><span class="sxs-lookup"><span data-stu-id="295e2-236">Identity : Global</span></span>

<span data-ttu-id="295e2-237">Descritivo</span><span class="sxs-lookup"><span data-stu-id="295e2-237">Description :</span></span>

<span data-ttu-id="295e2-238">ArchiveInternal: false</span><span class="sxs-lookup"><span data-stu-id="295e2-238">ArchiveInternal : False</span></span>

<span data-ttu-id="295e2-239">ArchiveExternal: false</span><span class="sxs-lookup"><span data-stu-id="295e2-239">ArchiveExternal : False</span></span>

<span data-ttu-id="295e2-240">Observe que, por padrão, o arquivamento interno e externo está desabilitado em uma política de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="295e2-240">Note that, by default, both internal and external archiving are disabled in an archiving policy.</span></span>

</div>

<div>

## <a name="check-cdr-settings"></a><span data-ttu-id="295e2-241">Verificar as configurações do CDR</span><span class="sxs-lookup"><span data-stu-id="295e2-241">Check CDR settings</span></span>

<span data-ttu-id="295e2-242">Verifique as configurações de CDR (registro de detalhes de chamadas) para gravação ponto a ponto, conferência e detalhes de chamadas de voz.</span><span class="sxs-lookup"><span data-stu-id="295e2-242">Check Call Detail Record (CDR) settings for peer-to-peer, conferencing, and Voice call detail recording.</span></span> <span data-ttu-id="295e2-243">Informações detalhadas sobre as configurações do CDR podem ser retornadas usando o cmdlet **Get-CsCdrConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="295e2-243">Detailed information about your CDR settings can be returned by using the **Get-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="295e2-244">Por exemplo, esse comando retorna informações sobre a coleção global de definições de configuração de CDR:</span><span class="sxs-lookup"><span data-stu-id="295e2-244">For example, this command returns information about the global collection of CDR configuration settings:</span></span>

`Get-CsCdrConfiguration -Identity "Global"`

<span data-ttu-id="295e2-245">Como a CDR também pode ser configurada no escopo do site, talvez você também queira executar esse comando, que retorna informações sobre todas as definições de configuração de CDR:</span><span class="sxs-lookup"><span data-stu-id="295e2-245">Because CDR can also be configured at the site scope, you might also want to run this command, which returns information about all the CDR configuration settings:</span></span>

`Get-CsCdrConfiguration`

<span data-ttu-id="295e2-246">O cmdlet Get-CsCdrConfiguration retorna informações parecidas com isso para cada coleção de definições de configuração de CDR:</span><span class="sxs-lookup"><span data-stu-id="295e2-246">The Get-CsCdrConfiguration cmdlet returns information similar to this for each collection of CDR configuration settings:</span></span>

<span data-ttu-id="295e2-247">Identidade: global</span><span class="sxs-lookup"><span data-stu-id="295e2-247">Identity : Global</span></span>

<span data-ttu-id="295e2-248">EnableCDR: true</span><span class="sxs-lookup"><span data-stu-id="295e2-248">EnableCDR : True</span></span>

<span data-ttu-id="295e2-249">EnablePurging: true</span><span class="sxs-lookup"><span data-stu-id="295e2-249">EnablePurging : True</span></span>

<span data-ttu-id="295e2-250">KeepCallDetailForDays: 60</span><span class="sxs-lookup"><span data-stu-id="295e2-250">KeepCallDetailForDays : 60</span></span>

<span data-ttu-id="295e2-251">KeepErrorReportForDays: 60</span><span class="sxs-lookup"><span data-stu-id="295e2-251">KeepErrorReportForDays : 60</span></span>

<span data-ttu-id="295e2-252">PurgeHourOfDay: 2</span><span class="sxs-lookup"><span data-stu-id="295e2-252">PurgeHourOfDay : 2</span></span>

<span data-ttu-id="295e2-253">Informações semelhantes podem ser retornadas para monitoramento de QoE usando o cmdlet Get-CsQoEConfiguration.</span><span class="sxs-lookup"><span data-stu-id="295e2-253">Similar information can be returned for QoE monitoring by using the Get-CsQoEConfiguration cmdlet.</span></span> <span data-ttu-id="295e2-254">Por exemplo, esse comando retorna informações sobre a coleção global de definições de configuração de QoE:</span><span class="sxs-lookup"><span data-stu-id="295e2-254">For example, this command returns information about the global collection of QoE configuration settings:</span></span>

`Get-QoEConfiguration -Identity "Global"`

<span data-ttu-id="295e2-255">Essas informações serão parecidas com isso:</span><span class="sxs-lookup"><span data-stu-id="295e2-255">That information will resemble this:</span></span>

<span data-ttu-id="295e2-256">Identidade: global</span><span class="sxs-lookup"><span data-stu-id="295e2-256">Identity : Global</span></span>

<span data-ttu-id="295e2-257">ExternalConsumerIssuedCertId :</span><span class="sxs-lookup"><span data-stu-id="295e2-257">ExternalConsumerIssuedCertId :</span></span>

<span data-ttu-id="295e2-258">EnablePurging: true</span><span class="sxs-lookup"><span data-stu-id="295e2-258">EnablePurging : True</span></span>

<span data-ttu-id="295e2-259">KeepQoEDataForDays: 60</span><span class="sxs-lookup"><span data-stu-id="295e2-259">KeepQoEDataForDays : 60</span></span>

<span data-ttu-id="295e2-260">PurgeHourOfDay: 1</span><span class="sxs-lookup"><span data-stu-id="295e2-260">PurgeHourOfDay : 1</span></span>

<span data-ttu-id="295e2-261">EnableExternalConsumer: false</span><span class="sxs-lookup"><span data-stu-id="295e2-261">EnableExternalConsumer : False</span></span>

<span data-ttu-id="295e2-262">ExternalConsumerName :</span><span class="sxs-lookup"><span data-stu-id="295e2-262">ExternalConsumerName :</span></span>

<span data-ttu-id="295e2-263">ExternalConsumerURL :</span><span class="sxs-lookup"><span data-stu-id="295e2-263">ExternalConsumerURL :</span></span>

<span data-ttu-id="295e2-264">EnableQoE: true</span><span class="sxs-lookup"><span data-stu-id="295e2-264">EnableQoE : True</span></span>

<span data-ttu-id="295e2-265">Se você quiser comparar as configurações atuais de CDR com as configurações de CDR padrão, os valores padrão podem ser revisados executando este comando:</span><span class="sxs-lookup"><span data-stu-id="295e2-265">If you want to compare your current CDR settings with the default CDR settings, the default values can be reviewed by running this command:</span></span>

`New-CsCdrConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="295e2-266">Da mesma forma, os valores padrão para monitoramento de QoE podem ser recuperados usando este comando:</span><span class="sxs-lookup"><span data-stu-id="295e2-266">Likewise, the default values for QoE monitoring can be retrieved by using this command:</span></span>

`New-CsQoEConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="295e2-267">Você também pode retornar o FQDN dos seus servidores de monitoração executando este comando:</span><span class="sxs-lookup"><span data-stu-id="295e2-267">You can also return the FQDN of your Monitoring servers by running this command:</span></span>

`Get-CsService -MonitoringServer`

</div>

<div>

## <a name="check-voice-settings"></a><span data-ttu-id="295e2-268">Verificar as configurações de voz</span><span class="sxs-lookup"><span data-stu-id="295e2-268">Check voice settings</span></span>

<span data-ttu-id="295e2-269">As configurações de voz geralmente importantes para os administradores estão contidas em políticas de voz e rotas de voz: as políticas de voz contêm as configurações que determinam os recursos expostos a usuários individuais (como a capacidade de encaminhar ou transferir chamadas), enquanto as rotas de voz determinam como as chamadas (e se) são roteadas pelo PSTN.</span><span class="sxs-lookup"><span data-stu-id="295e2-269">The voice settings typically important to administrators are contained in voice policies and voice routes: voice policies contain the settings that determine the capabilities exposed to individual users (such as the ability to forward or transfer calls), while voice routes determine how (and if) calls are routed across the PSTN.</span></span>

<span data-ttu-id="295e2-270">As informações da política de voz podem ser recuperadas usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="295e2-270">Voice policy information can be retrieved by using Windows PowerShell.</span></span> <span data-ttu-id="295e2-271">Por exemplo, esse comando retorna informações sobre a política de voz global:</span><span class="sxs-lookup"><span data-stu-id="295e2-271">For example, this command returns information about the global voice policy:</span></span>

`Get-CsVoicePolicy -Identity "Global"`

<span data-ttu-id="295e2-272">E esse comando retorna informações sobre todas as políticas de voz configuradas para uso na organização:</span><span class="sxs-lookup"><span data-stu-id="295e2-272">And this command returns information about all the voice policies configured for use in the organization:</span></span>

`Get-CsVoicePolicy`

<span data-ttu-id="295e2-273">As informações retornadas pelo cmdlet Get-CsVoicePolicy são semelhantes às seguintes:</span><span class="sxs-lookup"><span data-stu-id="295e2-273">The information returned by the Get-CsVoicePolicy cmdlet resembles the following:</span></span>

<span data-ttu-id="295e2-274">Identidade: global</span><span class="sxs-lookup"><span data-stu-id="295e2-274">Identity : Global</span></span>

<span data-ttu-id="295e2-275">PstnUsages : {}</span><span class="sxs-lookup"><span data-stu-id="295e2-275">PstnUsages : {}</span></span>

<span data-ttu-id="295e2-276">Descritivo</span><span class="sxs-lookup"><span data-stu-id="295e2-276">Description :</span></span>

<span data-ttu-id="295e2-277">AllowSimulRing: true</span><span class="sxs-lookup"><span data-stu-id="295e2-277">AllowSimulRing : True</span></span>

<span data-ttu-id="295e2-278">AllowCallForwarding: true</span><span class="sxs-lookup"><span data-stu-id="295e2-278">AllowCallForwarding : True</span></span>

<span data-ttu-id="295e2-279">AllowPSTNReRouting: true</span><span class="sxs-lookup"><span data-stu-id="295e2-279">AllowPSTNReRouting : True</span></span>

<span data-ttu-id="295e2-280">Nome: DefaultPolicy</span><span class="sxs-lookup"><span data-stu-id="295e2-280">Name : DefaultPolicy</span></span>

<span data-ttu-id="295e2-281">EnableDelegation: true</span><span class="sxs-lookup"><span data-stu-id="295e2-281">EnableDelegation : True</span></span>

<span data-ttu-id="295e2-282">EnableTeamCall: true</span><span class="sxs-lookup"><span data-stu-id="295e2-282">EnableTeamCall : True</span></span>

<span data-ttu-id="295e2-283">EnableCallTransfer: true</span><span class="sxs-lookup"><span data-stu-id="295e2-283">EnableCallTransfer : True</span></span>

<span data-ttu-id="295e2-284">EnableCallPark: false</span><span class="sxs-lookup"><span data-stu-id="295e2-284">EnableCallPark : False</span></span>

<span data-ttu-id="295e2-285">EnableMaliciousCallTracing: false</span><span class="sxs-lookup"><span data-stu-id="295e2-285">EnableMaliciousCallTracing : False</span></span>

<span data-ttu-id="295e2-286">EnableBWPolicyOverride: false</span><span class="sxs-lookup"><span data-stu-id="295e2-286">EnableBWPolicyOverride : False</span></span>

<span data-ttu-id="295e2-287">PreventPSTNTollBypass: false</span><span class="sxs-lookup"><span data-stu-id="295e2-287">PreventPSTNTollBypass : False</span></span>

<span data-ttu-id="295e2-288">Você também pode criar consultas que retornaram um subconjunto de suas políticas de voz.</span><span class="sxs-lookup"><span data-stu-id="295e2-288">You can also create queries that returned a subset of your voice policies.</span></span> <span data-ttu-id="295e2-289">Por exemplo, esse comando retorna todas as políticas de voz que permitem o encaminhamento de chamadas:</span><span class="sxs-lookup"><span data-stu-id="295e2-289">For example, this command returns all the voice policies that allow call forwarding:</span></span>

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $True}`

<span data-ttu-id="295e2-290">E esse comando retorna todas as políticas de voz que não permitem o encaminhamento de chamadas:</span><span class="sxs-lookup"><span data-stu-id="295e2-290">And this command returns all the voice policies that don’t allow call forwarding:</span></span>

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $False}`

<span data-ttu-id="295e2-291">No Windows PowerShell, use o cmdlet Get-CsVoiceRouting para retornar informações sobre suas rotas de voz:</span><span class="sxs-lookup"><span data-stu-id="295e2-291">In Windows PowerShell, use the Get-CsVoiceRouting cmdlet to return information about your voice routes:</span></span>

`Get-CsVoiceRoute`

<span data-ttu-id="295e2-292">Esse comando retorna informações como esta para todas as rotas de voz:</span><span class="sxs-lookup"><span data-stu-id="295e2-292">That command returns information such as this for all the voice routes:</span></span>

<span data-ttu-id="295e2-293">Identidade: LocalRoute</span><span class="sxs-lookup"><span data-stu-id="295e2-293">Identity : LocalRoute</span></span>

<span data-ttu-id="295e2-294">Prioridade: 0</span><span class="sxs-lookup"><span data-stu-id="295e2-294">Priority : 0</span></span>

<span data-ttu-id="295e2-295">Descritivo</span><span class="sxs-lookup"><span data-stu-id="295e2-295">Description :</span></span>

<span data-ttu-id="295e2-296">NumberPattern: ^ ( \\ + 1 \[ 0-9 \] {10} ) $</span><span class="sxs-lookup"><span data-stu-id="295e2-296">NumberPattern : ^(\\+1\[0-9\]{10})$</span></span>

<span data-ttu-id="295e2-297">PstnUsages : {}</span><span class="sxs-lookup"><span data-stu-id="295e2-297">PstnUsages : {}</span></span>

<span data-ttu-id="295e2-298">PstnGatewayList : {}</span><span class="sxs-lookup"><span data-stu-id="295e2-298">PstnGatewayList : {}</span></span>

<span data-ttu-id="295e2-299">Nome: LocalRoute</span><span class="sxs-lookup"><span data-stu-id="295e2-299">Name : LocalRoute</span></span>

<span data-ttu-id="295e2-300">SuppressCallerId :</span><span class="sxs-lookup"><span data-stu-id="295e2-300">SuppressCallerId :</span></span>

<span data-ttu-id="295e2-301">AlternateCallerId :</span><span class="sxs-lookup"><span data-stu-id="295e2-301">AlternateCallerId :</span></span>

<span data-ttu-id="295e2-302">O Lync Server permite criar rotas de voz que não têm um uso PSTN e não especificam um gateway PSTN.</span><span class="sxs-lookup"><span data-stu-id="295e2-302">Lync Server allows you to create voice routes that do not have a PSTN usage and do not specify a PSTN gateway.</span></span> <span data-ttu-id="295e2-303">No entanto, você não pode realmente rotear chamadas por uma rota de voz que não tenha esses dois valores de propriedade configurados.</span><span class="sxs-lookup"><span data-stu-id="295e2-303">However, you can't actually route calls over a voice route that does not have these two property values configured.</span></span> <span data-ttu-id="295e2-304">Por isso, talvez seja útil executar esse comando periodicamente, que retorna a identidade de qualquer rota de voz que não tenha um uso PSTN:</span><span class="sxs-lookup"><span data-stu-id="295e2-304">Because of that, you might find it useful to periodically run this command, which returns the identity of any voice route that does not have a PSTN usage:</span></span>

`Get-CsVoiceRoute | Where-Object {$_.PstnUsages -eq $Null} | Select-Object Identity`

<span data-ttu-id="295e2-305">Da mesma forma, esse comando retorna a identidade de qualquer rota de voz que não tenha sido configurada para ter um gateway PSTN:</span><span class="sxs-lookup"><span data-stu-id="295e2-305">Similarly, this command returns the identity of any voice route that has not been configured to have a PSTN gateway:</span></span>

`Get-CsVoiceRoute | Where-Object {$_.PstnGatewayList -eq $Null}} | Select-Object Identity`

</div>

<div>

## <a name="check-conferencing-attendant-settings"></a><span data-ttu-id="295e2-306">Verificar as configurações do atendedor de conferências</span><span class="sxs-lookup"><span data-stu-id="295e2-306">Check Conferencing Attendant settings</span></span>

<span data-ttu-id="295e2-307">Verifique as configurações do atendedor de conferências para conferências discadas PSTN.</span><span class="sxs-lookup"><span data-stu-id="295e2-307">Check conferencing Attendant settings for PSTN dial-in conferencing.</span></span> <span data-ttu-id="295e2-308">As configurações do atendedor de conferência só podem ser recuperadas usando o cmdlet **Get-CsDialInConferencingConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="295e2-308">Conferencing Attendant settings can only be retrieved by using the **Get-CsDialInConferencingConfiguration** cmdlet.</span></span> <span data-ttu-id="295e2-309">Essas configurações não estão disponíveis no painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="295e2-309">These settings are not available in the Lync Server Control Panel.</span></span> <span data-ttu-id="295e2-310">Para exibir as configurações do atendedor de conferência, use um comando do Windows PowerShell semelhante ao seguinte, que retorna a coleção global das configurações do atendedor de conferência:</span><span class="sxs-lookup"><span data-stu-id="295e2-310">To view your Conferencing Attendant settings, use a Windows PowerShell command similar to the following, which returns the global collection of Conferencing Attendant settings:</span></span>

`Get-CsDialInConferencingConfiguration -Identity "Global"`

<span data-ttu-id="295e2-311">Observe que as configurações do atendedor de conferências também podem ser configuradas no escopo do site.</span><span class="sxs-lookup"><span data-stu-id="295e2-311">Note that Conferencing Attendant settings can also be configured at the site scope.</span></span> <span data-ttu-id="295e2-312">Para retornar informações sobre todas as configurações do atendedor de conferência, use este comando em vez disso:</span><span class="sxs-lookup"><span data-stu-id="295e2-312">To return information about all the Conferencing Attendant settings, use this command instead:</span></span>

`Get-CsDialInConferencingConfiguration`

<span data-ttu-id="295e2-313">O cmdlet Get-CsDialInConferencingConfiguration retorna dados semelhantes a este:</span><span class="sxs-lookup"><span data-stu-id="295e2-313">The Get-CsDialInConferencingConfiguration cmdlet returns data similar to this:</span></span>

<span data-ttu-id="295e2-314">Identidade: global</span><span class="sxs-lookup"><span data-stu-id="295e2-314">Identity : Global</span></span>

<span data-ttu-id="295e2-315">EntryExitAnnouncementsType : UseNames</span><span class="sxs-lookup"><span data-stu-id="295e2-315">EntryExitAnnouncementsType : UseNames</span></span>

<span data-ttu-id="295e2-316">EnableNameRecording: true</span><span class="sxs-lookup"><span data-stu-id="295e2-316">EnableNameRecording : True</span></span>

<span data-ttu-id="295e2-317">EntryExitAnnouncementsEnabledByDefault: false</span><span class="sxs-lookup"><span data-stu-id="295e2-317">EntryExitAnnouncementsEnabledByDefault : False</span></span>

<span data-ttu-id="295e2-318">Se EntryExitAnnouncementsEnabledByDefault estiver definido como false, isso significa que os comunicados de conferência estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="295e2-318">If EntryExitAnnouncementsEnabledByDefault is set to False, that means the conferencing announcements are disabled.</span></span> <span data-ttu-id="295e2-319">Para habilitar os comunicados de entrada e saída, execute um comando do Windows PowerShell semelhante a este:</span><span class="sxs-lookup"><span data-stu-id="295e2-319">To enable entry and exit announcements, run a Windows PowerShell command similar to this:</span></span>

`Set-CsDialInConferencingConfiguration -Identity "Global" -EntryExitAnnouncementsEnabledByDefault $True`

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="295e2-320">Confira também</span><span class="sxs-lookup"><span data-stu-id="295e2-320">See Also</span></span>


[<span data-ttu-id="295e2-321">Get-CsSipDomain</span><span class="sxs-lookup"><span data-stu-id="295e2-321">Get-CsSipDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsSipDomain)  
[<span data-ttu-id="295e2-322">Get-CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="295e2-322">Get-CsMeetingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingConfiguration)  
[<span data-ttu-id="295e2-323">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="295e2-323">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="295e2-324">Get-CsAccessEdgeConfiguration</span><span class="sxs-lookup"><span data-stu-id="295e2-324">Get-CsAccessEdgeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAccessEdgeConfiguration)  
[<span data-ttu-id="295e2-325">Get-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="295e2-325">Get-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsExternalAccessPolicy)  
[<span data-ttu-id="295e2-326">Get-CsArchivingConfiguration</span><span class="sxs-lookup"><span data-stu-id="295e2-326">Get-CsArchivingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsArchivingConfiguration)  
[<span data-ttu-id="295e2-327">Get-CsCdrConfiguration</span><span class="sxs-lookup"><span data-stu-id="295e2-327">Get-CsCdrConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCdrConfiguration)  
[<span data-ttu-id="295e2-328">Get-CsQoEConfiguration</span><span class="sxs-lookup"><span data-stu-id="295e2-328">Get-CsQoEConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsQoEConfiguration)  
[<span data-ttu-id="295e2-329">Get-CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="295e2-329">Get-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicePolicy)  
[<span data-ttu-id="295e2-330">Get-CsVoiceRoute</span><span class="sxs-lookup"><span data-stu-id="295e2-330">Get-CsVoiceRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoiceRoute)  
[<span data-ttu-id="295e2-331">Get-CsDialInConferencingConfiguration</span><span class="sxs-lookup"><span data-stu-id="295e2-331">Get-CsDialInConferencingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDialInConferencingConfiguration)  
  

<span data-ttu-id="295e2-332"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="295e2-332"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

