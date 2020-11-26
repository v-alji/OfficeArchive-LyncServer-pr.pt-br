---
title: Configurando as várias políticas
description: Configurar as diversas políticas.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configuring the Various Policies
ms:assetid: e3b3cbda-7c17-470b-acb0-82fdcc473184
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945610(v=OCS.15)
ms:contentKeyID: 51541436
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 746d299ac605c7dfe89a957246d47309dfbc0a5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440040"
---
# <a name="configuring-the-various-policies"></a><span data-ttu-id="4daa1-103">Configurando as várias políticas</span><span class="sxs-lookup"><span data-stu-id="4daa1-103">Configuring the Various Policies</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4daa1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4daa1-104">

<span> </span></span></span>

<span data-ttu-id="4daa1-105">_**Tópico da última modificação:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="4daa1-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<div>

<span data-ttu-id="4daa1-106">Aqui estão as várias políticas que você pode configurar na sua topologia do Lync Server 2013, antes de executar a ferramenta de stress e desempenho do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4daa1-106">Here are the various policies that you can configure in your Lync Server 2013 topology, prior to running the Lync Server 2013 Stress and Performance Tool.</span></span>

<div>

## <a name="configuring-the-archiving-policy"></a><span data-ttu-id="4daa1-107">Configurar a política de arquivamento</span><span class="sxs-lookup"><span data-stu-id="4daa1-107">Configuring the Archiving Policy</span></span>

<span data-ttu-id="4daa1-108">Consulte o ArchivingPolicy.ps1 de script de exemplo.</span><span class="sxs-lookup"><span data-stu-id="4daa1-108">See the example script ArchivingPolicy.ps1.</span></span> <span data-ttu-id="4daa1-109">Você só precisará usar esse script se um servidor de arquivamento estiver implantado na sua topologia.</span><span class="sxs-lookup"><span data-stu-id="4daa1-109">You need to use this script only if an Archiving Server is deployed in your topology.</span></span> <span data-ttu-id="4daa1-110">Para obter detalhes, consulte a documentação do Lync Server 2013 e a ajuda do cmdlet para [arquivamento e monitoramento de cmdlets no Lync Server 2013](https://technet.microsoft.com/library/gg415629\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="4daa1-110">For details, see the Lync Server 2013 documentation and cmdlet Help for [Archiving and Monitoring cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415629\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-conferencing-policy"></a><span data-ttu-id="4daa1-111">Configurar a política de conferência</span><span class="sxs-lookup"><span data-stu-id="4daa1-111">Configuring the Conferencing Policy</span></span>

<span data-ttu-id="4daa1-112">Consulte o MeetingPolicy.ps1 de script de exemplo.</span><span class="sxs-lookup"><span data-stu-id="4daa1-112">See the example script MeetingPolicy.ps1.</span></span> <span data-ttu-id="4daa1-113">Para obter detalhes, consulte a documentação do Lync Server 2013 e a ajuda do cmdlet para [cmdlets de Webconferência no Lync server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="4daa1-113">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Web conferencing cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-contacts-policy"></a><span data-ttu-id="4daa1-114">Configurando a política de contatos</span><span class="sxs-lookup"><span data-stu-id="4daa1-114">Configuring the Contacts Policy</span></span>

<span data-ttu-id="4daa1-115">Consulte o exemplo ContactsPolicy.ps1.</span><span class="sxs-lookup"><span data-stu-id="4daa1-115">See the example ContactsPolicy.ps1.</span></span> <span data-ttu-id="4daa1-116">Para obter detalhes, consulte a documentação do Lync Server 2013 e a ajuda do cmdlet para os [cmdlets de presença e mensagens instantâneas no Lync server 2013](https://technet.microsoft.com/library/gg398611\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="4daa1-116">For details, see the Lync Server 2013 documentation and the cmdlet Help for [IM and presence cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg398611\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-federation-policy"></a><span data-ttu-id="4daa1-117">Configurando a política de Federação</span><span class="sxs-lookup"><span data-stu-id="4daa1-117">Configuring the Federation Policy</span></span>

<span data-ttu-id="4daa1-118">Consulte o exemplo FederationPolicy.ps1.</span><span class="sxs-lookup"><span data-stu-id="4daa1-118">See the example FederationPolicy.ps1.</span></span> <span data-ttu-id="4daa1-119">Para obter detalhes, consulte a documentação do Lync Server 2013 e a ajuda do cmdlet para [cmdlets do servidor de borda no Lync server 2013](https://technet.microsoft.com/library/gg415635\(v=ocs.15\)) e [cmdlets de acesso externo e Federação no Lync Server 2013](https://technet.microsoft.com/library/gg415651\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="4daa1-119">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Edge Server cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415635\(v=ocs.15\)) and [Federation and external access cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415651\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-call-admission-control-policy"></a><span data-ttu-id="4daa1-120">Configurando a política de controle de admissão de chamadas</span><span class="sxs-lookup"><span data-stu-id="4daa1-120">Configuring the Call Admission Control Policy</span></span>

<span data-ttu-id="4daa1-121">Consulte o exemplo BandwidthPolicy.ps1.</span><span class="sxs-lookup"><span data-stu-id="4daa1-121">See the example BandwidthPolicy.ps1.</span></span> <span data-ttu-id="4daa1-122">Para obter detalhes, consulte a [visão geral da documentação do Lync Server 2013 do controle de admissão de chamadas no Lync server 2013](https://technet.microsoft.com/library/gg398529\(v=ocs.15\)) e a ajuda do cmdlet para [cmdlets de controle de admissão de chamadas no Lync Server 2013](https://technet.microsoft.com/library/gg415676\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="4daa1-122">For details, see the Lync Server 2013 documentation [Overview of call admission control in Lync Server 2013](https://technet.microsoft.com/library/gg398529\(v=ocs.15\)) and the cmdlet Help for [Call admission control cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415676\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-voice-routing-rules"></a><span data-ttu-id="4daa1-123">Configurando as regras de roteamento de voz</span><span class="sxs-lookup"><span data-stu-id="4daa1-123">Configuring the Voice Routing Rules</span></span>

<span data-ttu-id="4daa1-124">Consulte o exemplo RoutingRules.ps1.</span><span class="sxs-lookup"><span data-stu-id="4daa1-124">See the example RoutingRules.ps1.</span></span> <span data-ttu-id="4daa1-125">Ao configurar as regras de roteamento de voz, anote o contexto do telefone (ou seja, o perfil do/Location ou/SimpleName) e os códigos de área interna/externa para que você possa especificá-los ao criar usuários e durante a configuração do LyncPerfTool (especificamente para PSTN-UC e UC-PSTN).</span><span class="sxs-lookup"><span data-stu-id="4daa1-125">When you configure the voice routing rules, take note of the Phone Context (that is, /Location Profile or /SimpleName) and Internal/External Area Codes so that you can specify them when creating users and during LyncPerfTool configuration (specifically for PSTN-UC and UC-PSTN).</span></span> <span data-ttu-id="4daa1-126">Por exemplo, o parâmetro SimpleName na chamada para o cmdlet **New-CsDialPlan** no exemplo de RoutingRules.ps1 deve ser usado para o valor LocationProfile na figura a seguir de UserProfileGenerator.exe.</span><span class="sxs-lookup"><span data-stu-id="4daa1-126">For example, the SimpleName parameter in the call to the **New-CsDialPlan** cmdlet in the RoutingRules.ps1 example should be used for the LocationProfile value in the following figure of UserProfileGenerator.exe.</span></span>

<span data-ttu-id="4daa1-127">![Regra de roteamento de voz de exemplo.](images/JJ945610.9f34d971-4ed0-4a4c-b101-086a91c4578c(OCS.15).jpg "Regra de roteamento de voz de exemplo.")</span><span class="sxs-lookup"><span data-stu-id="4daa1-127">![Sample voice routing rule.](images/JJ945610.9f34d971-4ed0-4a4c-b101-086a91c4578c(OCS.15).jpg "Sample voice routing rule.")</span></span>

<span data-ttu-id="4daa1-128">Para obter detalhes, consulte a documentação do Lync Server 2013 e a ajuda do cmdlet para [cmdlets do Enterprise Voice no Lync Server 2013](https://technet.microsoft.com/library/gg415658\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="4daa1-128">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Enterprise Voice cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415658\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-conferencing-attendant-application"></a><span data-ttu-id="4daa1-129">Configurando o aplicativo de assistente de conferência</span><span class="sxs-lookup"><span data-stu-id="4daa1-129">Configuring Conferencing Attendant application</span></span>

<span data-ttu-id="4daa1-130">Consulte o exemplo ConferenceAutoAttendantConfiguration.ps1.</span><span class="sxs-lookup"><span data-stu-id="4daa1-130">See the example ConferenceAutoAttendantConfiguration.ps1.</span></span> <span data-ttu-id="4daa1-131">Anote o número de telefone ConferencingAutoAttendant (1121111111, por padrão), para que você possa digitá-lo na ferramenta de configuração da ferramenta LyncPerf para geração de configuração.</span><span class="sxs-lookup"><span data-stu-id="4daa1-131">Take note of the ConferencingAutoAttendant phone number (1121111111, by default), so that you can type it into the LyncPerf Tool Configuration tool for configuration generation.</span></span>

<span data-ttu-id="4daa1-132">![Configurando o aplicativo assistente de conferência](images/JJ945610.0618a22f-27a9-423a-9085-d2bf71e82db6(OCS.15).jpg "Configurando o aplicativo assistente de conferência")</span><span class="sxs-lookup"><span data-stu-id="4daa1-132">![Configuring the Conferencing Attendant application](images/JJ945610.0618a22f-27a9-423a-9085-d2bf71e82db6(OCS.15).jpg "Configuring the Conferencing Attendant application")</span></span>

<span data-ttu-id="4daa1-133">Para obter detalhes, consulte a documentação do Lync Server 2013 e a ajuda do cmdlet para [cmdlets de Webconferência no Lync server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)) e [cmdlets de conferência discada no Lync Server 2013](https://technet.microsoft.com/library/gg415630\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="4daa1-133">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Web conferencing cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)) and [Dial-in conferencing cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415630\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-lync-server-call-park-service"></a><span data-ttu-id="4daa1-134">Configurando o serviço de estacionamento de chamadas do Lync Server</span><span class="sxs-lookup"><span data-stu-id="4daa1-134">Configuring Lync Server Call Park Service</span></span>

<span data-ttu-id="4daa1-135">O parque de chamadas está desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="4daa1-135">Call Park is disabled by default.</span></span> <span data-ttu-id="4daa1-136">Consulte o exemplo CallParkConfiguration.ps1.</span><span class="sxs-lookup"><span data-stu-id="4daa1-136">See the example CallParkConfiguration.ps1.</span></span> <span data-ttu-id="4daa1-137">Para obter detalhes, consulte a documentação do Lync Server 2013 e a ajuda do cmdlet para os [cmdlets do aplicativo de estacionamento de chamada no Lync Server 2013](https://technet.microsoft.com/library/gg415639\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="4daa1-137">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Call Park application cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415639\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-emergency-calls"></a><span data-ttu-id="4daa1-138">Configurando chamadas de emergência</span><span class="sxs-lookup"><span data-stu-id="4daa1-138">Configuring Emergency Calls</span></span>

<span data-ttu-id="4daa1-139">Execute as etapas a seguir para configurar o teste de stress e desempenho para chamadas de emergência.</span><span class="sxs-lookup"><span data-stu-id="4daa1-139">Perform the following steps to configure stress and performance testing for emergency calls.</span></span>

1.  <span data-ttu-id="4daa1-140">Configurar uma rota de voz para chamadas de emergência.</span><span class="sxs-lookup"><span data-stu-id="4daa1-140">Set up a voice route for emergency calls.</span></span> <span data-ttu-id="4daa1-141">Consulte o script RoutingRules.ps1 sob o comentário "Route E911 to PSTN" para obter um exemplo de como configurar essa rota de voz.</span><span class="sxs-lookup"><span data-stu-id="4daa1-141">See the RoutingRules.ps1 script under the comment "Route E911 to PSTN" for an example of setting up this voice route.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="4daa1-142">O exemplo de comando em RoutingRules.ps1 tem um padrão de número que inclui o número 119 em vez de 911.</span><span class="sxs-lookup"><span data-stu-id="4daa1-142">The example command in RoutingRules.ps1 has a number pattern that includes the number 119 rather than 911.</span></span> <span data-ttu-id="4daa1-143">Evite usar o 911 (ou o seu número de emergência local real) para evitar chamadas acidentais para seus operadores de emergência locais durante o teste de carga.</span><span class="sxs-lookup"><span data-stu-id="4daa1-143">You should avoid using 911 (or your actual local emergency number) to prevent accidental calls to your local emergency operators during load testing.</span></span> <span data-ttu-id="4daa1-144">Essa configuração é somente para fins de simulação.</span><span class="sxs-lookup"><span data-stu-id="4daa1-144">This configuration is for simulation purposes only.</span></span>

    
    </div>

2.  <span data-ttu-id="4daa1-145">Para configurar endereços, preencha os valores na guia **Lis** no UserProvisioningTool, conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="4daa1-145">Configure addresses by filling in the values on the **LIS** tab in the UserProvisioningTool, as shown in the following figure.</span></span>
    
    <span data-ttu-id="4daa1-146">![Configurar o serviço de informações de localização.](images/JJ945610.8ac1faa1-e9f9-40d0-b8b7-b159f4f459f7(OCS.15).jpg "Configurar o serviço de informações de localização.")</span><span class="sxs-lookup"><span data-stu-id="4daa1-146">![Configuring the Location Information Service.](images/JJ945610.8ac1faa1-e9f9-40d0-b8b7-b159f4f459f7(OCS.15).jpg "Configuring the Location Information Service.")</span></span>  

3.  <span data-ttu-id="4daa1-147">Clique em **gerar arquivos Lis config**.</span><span class="sxs-lookup"><span data-stu-id="4daa1-147">Click **Generate LIS Config Files**.</span></span>

4.  <span data-ttu-id="4daa1-148">Arquivos CSV para portas, sub-redes, opções e pontos de acesso sem fio (WAPs) e um arquivo XML para a ferramenta de stress e desempenho do Lync Server 2013 são gerados.</span><span class="sxs-lookup"><span data-stu-id="4daa1-148">CSV files for ports, subnets, switches, and wireless access points (WAPs), and an XML file for the Lync Server 2013 Stress and Performance Tool, are generated.</span></span> <span data-ttu-id="4daa1-149">Os arquivos CSV devem ser usados como entradas (na mesma pasta) durante a configuração do LIS (serviço de informações de localização) com o script LisConfiguration.ps1.</span><span class="sxs-lookup"><span data-stu-id="4daa1-149">The CSV files are to be used as inputs (in the same folder) when configuring Location Information service (LIS) with the LisConfiguration.ps1 script.</span></span> <span data-ttu-id="4daa1-150">Mova o arquivo Locations0.xml gerado para a mesma pasta que o executável da ferramenta de desempenho e stress (LyncPerfTool.exe) do Lync Server 2013, que executará cenários de perfil de localização (plano de discagem).</span><span class="sxs-lookup"><span data-stu-id="4daa1-150">Move the generated Locations0.xml file to the same folder as the Lync Server 2013 Stress and Performance Tool executable (LyncPerfTool.exe), which will run location profile (dial plan) scenarios.</span></span>

</div>

<div>

## <a name="creating-enabling-configuring-and-disabling-users"></a><span data-ttu-id="4daa1-151">Criando, habilitando, Configurando e desabilitando usuários</span><span class="sxs-lookup"><span data-stu-id="4daa1-151">Creating, Enabling, Configuring and Disabling Users</span></span>

<span data-ttu-id="4daa1-152">Você deve criar todos os usuários antes de executar os scripts a seguir.</span><span class="sxs-lookup"><span data-stu-id="4daa1-152">You should create all your users before running the following scripts.</span></span> <span data-ttu-id="4daa1-153">Siga as instruções em [criar usuários e contatos](create-users-and-contacts.md) para criar usuários.</span><span class="sxs-lookup"><span data-stu-id="4daa1-153">Follow the instructions in [Create Users and Contacts](create-users-and-contacts.md) to create users.</span></span> <span data-ttu-id="4daa1-154">Para obter detalhes, consulte a documentação do cmdlet do Lync Server 2013 para os cmdlets [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)), [set-CsUser](https://technet.microsoft.com/library/gg398510\(v=ocs.15\))e [Disable-CsUser](https://technet.microsoft.com/library/gg398747\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="4daa1-154">For details, see the Lync Server 2013 cmdlet documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)), [Set-CsUser](https://technet.microsoft.com/library/gg398510\(v=ocs.15\)), and [Disable-CsUser](https://technet.microsoft.com/library/gg398747\(v=ocs.15\)) cmdlets.</span></span>

</div>

<div>

## <a name="configuring-response-group-application"></a><span data-ttu-id="4daa1-155">Configurando o aplicativo grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="4daa1-155">Configuring Response Group application</span></span>

<span data-ttu-id="4daa1-156">Consulte o exemplo ResponseGroupConfiguration.ps1.</span><span class="sxs-lookup"><span data-stu-id="4daa1-156">See the example ResponseGroupConfiguration.ps1.</span></span> <span data-ttu-id="4daa1-157">Para obter detalhes, consulte a documentação do Lync Server 2013 e a ajuda do cmdlet para os [cmdlets do aplicativo grupo de resposta no Lync Server 2013](https://technet.microsoft.com/library/gg415654\(v=ocs.15\)). Para revisar a configuração do aplicativo grupo de resposta, consulte `https://<poolfqdn>/RgsConfig/` , conforme mostrado na figura a seguir.</span><span class="sxs-lookup"><span data-stu-id="4daa1-157">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Response Group application cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415654\(v=ocs.15\)).To review the Response Group application configuration, see `https://<poolfqdn>/RgsConfig/`, as shown in the following figure.</span></span>

<span data-ttu-id="4daa1-158">![A ferramenta de configuração de grupo de resposta.](images/JJ945610.480a9440-2283-4533-98f8-86daaab4781c(OCS.15).jpg "A ferramenta de configuração de grupo de resposta.")</span><span class="sxs-lookup"><span data-stu-id="4daa1-158">![The Response Group Configuration Tool.](images/JJ945610.480a9440-2283-4533-98f8-86daaab4781c(OCS.15).jpg "The Response Group Configuration Tool.")</span></span>

<span data-ttu-id="4daa1-159"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4daa1-159"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

