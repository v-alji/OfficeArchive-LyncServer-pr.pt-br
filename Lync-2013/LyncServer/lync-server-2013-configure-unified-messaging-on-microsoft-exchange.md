---
title: 'Lync Server 2013: configurar a Unificação de mensagens no Microsoft Exchange'
description: 'Lync Server 2013: configurar a Unificação de mensagens no Microsoft Exchange.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure Unified Messaging on Microsoft Exchange
ms:assetid: 07547968-c59b-4dde-ace4-9fd286933759
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398129(v=OCS.15)
ms:contentKeyID: 48183311
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8db43bbe50061a1a044bdd34b637ba86f626ca85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390412"
---
# <a name="configure-unified-messaging-on-microsoft-exchange-for-lync-server-2013"></a><span data-ttu-id="fd841-103">Configurar a Unificação de mensagens no Microsoft Exchange para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fd841-103">Configure Unified Messaging on Microsoft Exchange for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fd841-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fd841-104">

<span> </span></span></span>

<span data-ttu-id="fd841-105">_**Tópico da última modificação:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="fd841-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="fd841-106">Este tópico descreve como configurar o Microsoft Exchange Unified Messaging (um) em um servidor do Microsoft Exchange para uso com o Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="fd841-106">This topic describes how to configure Exchange Unified Messaging (UM) on a Microsoft Exchange Server for use with Enterprise Voice.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fd841-107">Os exemplos de cmdlet neste tópico fornecem a sintaxe para a versão do Exchange 2007 do Shell de gerenciamento do Exchange.</span><span class="sxs-lookup"><span data-stu-id="fd841-107">The cmdlet examples in this topic provide syntax for the Exchange 2007 version of Exchange Management Shell.</span></span> <span data-ttu-id="fd841-108">Se você estiver executando o Exchange 2010 ou o Exchange 2013, consulte a documentação apropriada como referenciada.</span><span class="sxs-lookup"><span data-stu-id="fd841-108">If you are running Exchange 2010 or Exchange 2013, see the appropriate documentation as referenced.</span></span>



</div>

<div>

## <a name="to-configure-a-server-running-exchange-server-um"></a><span data-ttu-id="fd841-109">Para configurar um servidor que esteja executando o Exchange Server UM</span><span class="sxs-lookup"><span data-stu-id="fd841-109">To configure a server running Exchange Server UM</span></span>

1.  <span data-ttu-id="fd841-110">Crie um plano de discagem de URI (Uniform Resource Identifier) do UM protocolo SIP para cada um dos perfis de local de voz de sua empresa.</span><span class="sxs-lookup"><span data-stu-id="fd841-110">Create a UM Session Initiation Protocol (SIP) Uniform Resource Identifier (URI) dial plan for each of your Enterprise Voice location profiles.</span></span> <span data-ttu-id="fd841-111">Se você optar por usar o console de gerenciamento do Exchange, crie um novo plano de discagem com a configuração de segurança **protegida (preferencial)**.</span><span class="sxs-lookup"><span data-stu-id="fd841-111">If you choose to use the Exchange Management Console, create a new dial plan with the security setting **Secured (preferred)**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="fd841-112">Se você definir seu valor de configuração de segurança como <STRONG>SIP Secured</STRONG> para exigir criptografia somente para tráfego SIP, como recomendado anteriormente, observe que essa configuração de segurança em um plano de discagem é insuficiente se o pool de front-ends estiver configurado para exigir criptografia, o que significa que o pool requer criptografia para tráfego SIP e RTP.</span><span class="sxs-lookup"><span data-stu-id="fd841-112">If you set your security setting value to <STRONG>SIP Secured</STRONG> to require encryption for SIP traffic only, as previously recommended, note that this security setting on a dial plan is insufficient if the Front End pool is configured to require encryption, which means the pool requires encryption for both SIP and RTP traffic.</span></span> <span data-ttu-id="fd841-113">Quando o plano de discagem e as configurações de segurança do pool não forem compatíveis, todas as chamadas para o Exchange UM do pool de front-ends falharão, resultando em um erro, indicando que você tem uma "configuração de segurança incompatível".</span><span class="sxs-lookup"><span data-stu-id="fd841-113">When the dial plan and pool security settings are not compatible, all calls to Exchange UM from the Front End pool will fail, resulting in an error indicating that you have an "Incompatible security setting."</span></span>

    
    </div>
    
    <span data-ttu-id="fd841-114">Se você usar o Shell de gerenciamento do Exchange, digite:</span><span class="sxs-lookup"><span data-stu-id="fd841-114">If you use the Exchange Management Shell, type:</span></span>
    ```powershell
     New-UMDialPlan -Name <dial plan name> -UriType "SipName" -VoipSecurity <SIPSecured|Unsecured|Secured> -NumberOfDigitsInExtension <number of digits> -AccessTelephoneNumbers <access number in E.164 format>
    ```
    <span data-ttu-id="fd841-115">Para obter detalhes, consulte:</span><span class="sxs-lookup"><span data-stu-id="fd841-115">For details, see:</span></span>
    
      - <span data-ttu-id="fd841-116">Para o Office Communications Server 2007, consulte "como criar um plano de discagem de URI SIP de Unificação de mensagens" at [https://go.microsoft.com/fwlink/p/?LinkId=268632](https://go.microsoft.com/fwlink/p/?linkid=268632) e "New-UMDialplan: Exchange 2007 ajuda" em [https://go.microsoft.com/fwlink/p/?LinkId=268666](https://go.microsoft.com/fwlink/p/?linkid=268666) .</span><span class="sxs-lookup"><span data-stu-id="fd841-116">For Office Communications Server 2007, see "How to Create a Unified Messaging SIP URI Dial Plan" at [https://go.microsoft.com/fwlink/p/?LinkId=268632](https://go.microsoft.com/fwlink/p/?linkid=268632) and "New-UMDialplan: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268666](https://go.microsoft.com/fwlink/p/?linkid=268666).</span></span>
    
      - <span data-ttu-id="fd841-117">Para o Exchange 2010, consulte "criar um plano de discagem de UM" em [https://go.microsoft.com/fwlink/p/?LinkId=268674](https://go.microsoft.com/fwlink/p/?linkid=268674) e "novo-UMDialPlan: Exchange 2010 ajuda" em [https://go.microsoft.com/fwlink/p/?LinkId=268680](https://go.microsoft.com/fwlink/p/?linkid=268680) .</span><span class="sxs-lookup"><span data-stu-id="fd841-117">For Exchange 2010, see "Create a UM Dial Plan" at [https://go.microsoft.com/fwlink/p/?LinkId=268674](https://go.microsoft.com/fwlink/p/?linkid=268674) and "New-UMDialplan: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268680](https://go.microsoft.com/fwlink/p/?linkid=268680).</span></span>
    
      - <span data-ttu-id="fd841-118">Para o Exchange 2013, consulte "mensagens unificadas" em [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579) .</span><span class="sxs-lookup"><span data-stu-id="fd841-118">For Exchange 2013, see "Unified Messaging" at [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fd841-119">Não importa se você selecionou um nível de segurança do <STRONG>SIPSecured</STRONG> ou <STRONG>protegido</STRONG> depende se o SRTP (protocolo de transporte em tempo real seguro) está ativado ou desativado para criptografia de mídia.</span><span class="sxs-lookup"><span data-stu-id="fd841-119">Whether you select a security level of <STRONG>SIPSecured</STRONG> or <STRONG>Secured</STRONG> depends on whether secure real-time transport protocol (SRTP) is activated or deactivated for media encryption.</span></span> <span data-ttu-id="fd841-120">Para a integração do Lync Server 2010 com o Exchange UM, isso deve corresponder ao nível de criptografia na configuração de mídia do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fd841-120">For the Lync Server 2010 integration with Exchange UM, this should correspond to the encryption level in the Lync Server media configuration.</span></span> <span data-ttu-id="fd841-121">A configuração de mídia do Lync Server pode ser exibida executando o cmdlet <STRONG>Get-CsMediaConfiguration</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="fd841-121">The Lync Server media configuration can be viewed by running the <STRONG>Get-CsMediaConfiguration</STRONG> cmdlet.</span></span> <span data-ttu-id="fd841-122">Para obter detalhes, consulte Get-CsMediaConfiguration na documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fd841-122">For details, see Get-CsMediaConfiguration in the Lync Server Management Shell documentation.</span></span><BR><span data-ttu-id="fd841-123">Para obter detalhes sobre como selecionar a configuração de segurança de VoIP apropriada, consulte <A href="lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md">processo de implantação para integrar a Unificação de mensagens local e o Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="fd841-123">For details about selecting the appropriate VoIP Security setting, see <A href="lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</A>.</span></span>

    
    </div>

2.  <span data-ttu-id="fd841-124">Execute o cmdlet a seguir para obter o nome de domínio totalmente qualificado (FQDN) de cada plano de discagem do UM:</span><span class="sxs-lookup"><span data-stu-id="fd841-124">Run the following cmdlet to obtain the fully qualified domain name (FQDN) for each UM dial plan:</span></span>
    
    ```powershell
    (Get-UMDialPlan <dialplanname>).PhoneContext  
    ```
    
    <span data-ttu-id="fd841-125">Para obter detalhes, consulte:</span><span class="sxs-lookup"><span data-stu-id="fd841-125">For details, see:</span></span>
    
      - <span data-ttu-id="fd841-126">Para o Exchange 2007, consulte "Get-UMDialplan: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268678](https://go.microsoft.com/fwlink/p/?linkid=268678) .</span><span class="sxs-lookup"><span data-stu-id="fd841-126">For Exchange 2007, see "Get-UMDialplan: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268678](https://go.microsoft.com/fwlink/p/?linkid=268678).</span></span>
    
      - <span data-ttu-id="fd841-127">Para o Exchange 2010, consulte "Get-UMDialplan: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268679](https://go.microsoft.com/fwlink/p/?linkid=268679) .</span><span class="sxs-lookup"><span data-stu-id="fd841-127">For Exchange 2010, see "Get-UMDialplan: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268679](https://go.microsoft.com/fwlink/p/?linkid=268679).</span></span>
    
      - <span data-ttu-id="fd841-128">Para o Exchange 2013, consulte "mensagens unificadas" em [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579) .</span><span class="sxs-lookup"><span data-stu-id="fd841-128">For Exchange 2013, see "Unified Messaging" at [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579).</span></span>

3.  <span data-ttu-id="fd841-129">Grave o nome do plano de discagem de cada plano de discagem do UM.</span><span class="sxs-lookup"><span data-stu-id="fd841-129">Record the dial plan name of each UM dial plan.</span></span> <span data-ttu-id="fd841-130">Dependendo da sua versão do Exchange Server, talvez seja necessário usar o FQDN de cada nome de plano de discagem posteriormente como o nome de cada plano de discagem do Lync Server correspondente para que os nomes dos planos de discagem sejam correspondentes.</span><span class="sxs-lookup"><span data-stu-id="fd841-130">Depending on your version of Exchange Server, you may need to use the FQDN of each dial plan name later as the name of each UM dial plan’s corresponding Lync Server dial plan so that the dial plan names match.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fd841-131">Os nomes dos planos de discagem do Lync Server devem coincidir com nomes de plano de discagem do UM apenas se o plano de discagem do UM estiver sendo executado em uma versão do Exchange <EM>anterior</EM> ao Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="fd841-131">Lync Server dial plan names must match UM dial plan names only if the UM dial plan is running on a version of Exchange <EM>earlier</EM> than Exchange 2010 SP1.</span></span>

    
    </div>

4.  <span data-ttu-id="fd841-132">Adicione o plano de discagem ao servidor que executa o UM do Exchange da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fd841-132">Add the dial plan to the server running Exchange UM as follows:</span></span>
    
      - <span data-ttu-id="fd841-133">Se você optar por usar o console de gerenciamento do Exchange, poderá adicionar o plano de discagem na folha de propriedades do servidor.</span><span class="sxs-lookup"><span data-stu-id="fd841-133">If you choose to use the Exchange Management Console, you can add the dial plan from the property sheet for the server.</span></span> <span data-ttu-id="fd841-134">Para obter instruções específicas, consulte a documentação do produto Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fd841-134">For specific instructions, see the Exchange Server product documentation.</span></span>
        
        <span data-ttu-id="fd841-135">Para o Exchange 2007, consulte "como adicionar um servidor de Unificação de mensagens a um plano de discagem" em [https://go.microsoft.com/fwlink/p/?LinkId=268681](https://go.microsoft.com/fwlink/p/?linkid=268681) .</span><span class="sxs-lookup"><span data-stu-id="fd841-135">For Exchange 2007, see "How to Add Unified Messaging Server to a Dial Plan" at [https://go.microsoft.com/fwlink/p/?LinkId=268681](https://go.microsoft.com/fwlink/p/?linkid=268681).</span></span>
        
        <span data-ttu-id="fd841-136">Para o Exchange 2010, consulte "exibir ou configurar as propriedades de um servidor de um" em [https://go.microsoft.com/fwlink/p/?LinkId=268682](https://go.microsoft.com/fwlink/p/?linkid=268682) .</span><span class="sxs-lookup"><span data-stu-id="fd841-136">For Exchange 2010, see "View or Configure the Properties of a UM Server" at [https://go.microsoft.com/fwlink/p/?LinkId=268682](https://go.microsoft.com/fwlink/p/?linkid=268682).</span></span>
        
        <span data-ttu-id="fd841-137">Para o Exchange 2013, consulte "mensagens unificadas" em [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579) .</span><span class="sxs-lookup"><span data-stu-id="fd841-137">For Exchange 2013, see "Unified Messaging" at [https://go.microsoft.com/fwlink/p/?LinkID=266579](https://go.microsoft.com/fwlink/p/?linkid=266579).</span></span>
    
      - <span data-ttu-id="fd841-138">Se você usar o Shell de gerenciamento do Exchange, execute o seguinte para cada um dos seus servidores do Exchange UM:</span><span class="sxs-lookup"><span data-stu-id="fd841-138">If you use the Exchange Management Shell, run the following for each of your Exchange UM servers:</span></span>
        ```powershell
        $ums=get-umserver; 
        $dp=get-umdialplan -id <name of dial-plan created in step 1>; 
        $ums[0].DialPlans +=$dp.Identity; 
        set-umservice -instance $ums[0]
        ```
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fd841-139">Antes de executar a etapa a seguir, certifique-se de que todos os usuários do Enterprise Voice foram configurados com uma caixa de correio do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fd841-139">Before you perform the following step, make sure that all Enterprise Voice users have been configured with an Exchange Server mailbox.</span></span><BR><span data-ttu-id="fd841-140">Para o Exchange 2007, consulte a biblioteca do TechNet do Exchange Server 2007 em <A href="https://go.microsoft.com/fwlink/p/?linkid=268685">https://go.microsoft.com/fwlink/p/?LinkId=268685</A> .</span><span class="sxs-lookup"><span data-stu-id="fd841-140">For Exchange 2007, see the Exchange Server 2007 TechNet Library at <A href="https://go.microsoft.com/fwlink/p/?linkid=268685">https://go.microsoft.com/fwlink/p/?LinkId=268685</A>.</span></span><BR><span data-ttu-id="fd841-141">Para o Exchange 2010, consulte a biblioteca do TechNet do Exchange Server 2010 em <A href="https://go.microsoft.com/fwlink/p/?linkid=268686">https://go.microsoft.com/fwlink/p/?LinkId=268686</A> .</span><span class="sxs-lookup"><span data-stu-id="fd841-141">For Exchange 2010, see the Exchange Server 2010 TechNet Library at <A href="https://go.microsoft.com/fwlink/p/?linkid=268686">https://go.microsoft.com/fwlink/p/?LinkId=268686</A>.</span></span><BR><span data-ttu-id="fd841-142">Ao especificar uma política de caixa de correio para cada plano de discagem que você criou na etapa 1, selecione a política padrão ou uma que você tenha criado.</span><span class="sxs-lookup"><span data-stu-id="fd841-142">When specifying a mailbox policy for each dial plan that you created in step 1, select either the default policy or one that you have created.</span></span>

    
    </div>

5.  <span data-ttu-id="fd841-143">Navegue até \<Exchange installation directory\> \\ scripts e, se o Exchange estiver implantado em uma única floresta, digite:</span><span class="sxs-lookup"><span data-stu-id="fd841-143">Navigate to \<Exchange installation directory\>\\Scripts, and then if Exchange is deployed in a single forest, type:</span></span>
    ```console
    exchucutil.ps1
    ```
    <span data-ttu-id="fd841-144">Ou, se o Exchange estiver implantado em várias florestas, digite:</span><span class="sxs-lookup"><span data-stu-id="fd841-144">Or, if Exchange is deployed in multiple forests, type:</span></span>
    ```console
    exchucutil.ps1 -Forest:"<forest FQDN>"
    ```
    <span data-ttu-id="fd841-145">em que floresta FQDN especifica a floresta na qual o Lync Server é implantado.</span><span class="sxs-lookup"><span data-stu-id="fd841-145">where forest FQDN specifies the forest in which Lync Server is deployed.</span></span>
    
    <span data-ttu-id="fd841-146">Se você tiver um ou mais planos de discagem de UM associados a vários gateways IP, vá para a etapa 6.</span><span class="sxs-lookup"><span data-stu-id="fd841-146">If you have one or more UM dial plans that are associated with multiple IP gateways, continue to step 6.</span></span> <span data-ttu-id="fd841-147">Se seus planos de discagem estiverem associados a apenas um único gateway IP, pule a etapa 6.</span><span class="sxs-lookup"><span data-stu-id="fd841-147">If your dial plans are each associated with only a single IP gateway, skip step 6.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="fd841-148">Não se esqueça de reiniciar o serviço de <STRONG>front-end do Lync Server</STRONG> (rtcsrv.exe) <EM>após</EM> a execução do exchucutil.ps1.</span><span class="sxs-lookup"><span data-stu-id="fd841-148">Be sure to restart the <STRONG>Lync Server Front-End</STRONG> service (rtcsrv.exe) <EM>after</EM> you run exchucutil.ps1.</span></span> <span data-ttu-id="fd841-149">Caso contrário, o Lync Server não irá detectar a Unificação de mensagens na topologia.</span><span class="sxs-lookup"><span data-stu-id="fd841-149">Otherwise, Lync Server will not detect Unified Messaging in the topology.</span></span>

    
    </div>

6.  <span data-ttu-id="fd841-150">Usando o Shell de gerenciamento do Exchange ou o console de gerenciamento do Exchange, desabilite as chamadas de saída para todos, exceto um dos gateways IP associados a cada um dos planos de discagem.</span><span class="sxs-lookup"><span data-stu-id="fd841-150">Using either the Exchange Management Shell or Exchange Management Console, disable outbound calling for all but one of the IP gateways associated with each of your dial plans.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fd841-151">Esta etapa é necessária para garantir que as chamadas de saída do servidor que executam a Unificação de mensagens do Exchange Server sejam feitas a usuários externos (por exemplo, se o caso com cenários de reprodução sob o telefone) atravessará com confiança o firewall corporativo.</span><span class="sxs-lookup"><span data-stu-id="fd841-151">This step is necessary to make sure that outbound calls by the server running Exchange Server Unified Messaging to external users (for example, as is the case with play-on-phone scenarios) reliably traverse the corporate firewall.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="fd841-152">Ao selecionar o gateway IP de UM por meio do qual permitir chamadas feitas, escolha o que você pode manipular mais o tráfego.</span><span class="sxs-lookup"><span data-stu-id="fd841-152">When selecting the UM IP gateway through which to allow outgoing calls, choose the one that is likely to handle the most traffic.</span></span> <span data-ttu-id="fd841-153">Não permita o tráfego de saída por meio de um gateway IP que se conecta a um pool de diretores do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fd841-153">Do not allow outgoing traffic through an IP gateway that connects to a pool of Lync Server Directors.</span></span> <span data-ttu-id="fd841-154">Evite também pools em outro site central ou em um site de filial.</span><span class="sxs-lookup"><span data-stu-id="fd841-154">Also avoid pools in another central site or a branch site.</span></span> <span data-ttu-id="fd841-155">Você pode usar qualquer um dos seguintes métodos para impedir que chamadas feitas passem por um gateway IP:</span><span class="sxs-lookup"><span data-stu-id="fd841-155">You can use either of the following methods to block outgoing calls from passing through an IP gateway:</span></span>

    
    </div>
    
      - <span data-ttu-id="fd841-156">Se você usar o Shell de gerenciamento do Exchange, desabilite cada gateway IP executando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="fd841-156">If you use the Exchange Management Shell, disable each IP gateway by running the following command:</span></span>
        ```powershell
        Set-UMIPGateway <gatewayname> -OutcallsAllowed $false
        ```
        <span data-ttu-id="fd841-157">Para o Exchange 2007, consulte "Set-UMIPGateway: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268687](https://go.microsoft.com/fwlink/p/?linkid=268687) .</span><span class="sxs-lookup"><span data-stu-id="fd841-157">For Exchange 2007, see "Set-UMIPGateway: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268687](https://go.microsoft.com/fwlink/p/?linkid=268687).</span></span>
        
        <span data-ttu-id="fd841-158">Para o Exchange 2010, consulte "Set-UMIPGateway: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268688](https://go.microsoft.com/fwlink/p/?linkid=268688) .</span><span class="sxs-lookup"><span data-stu-id="fd841-158">For Exchange 2010, see "Set-UMIPGateway: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268688](https://go.microsoft.com/fwlink/p/?linkid=268688).</span></span>
    
      - <span data-ttu-id="fd841-159">Se você usar o console de gerenciamento do Exchange, desmarque a caixa de seleção **Permitir chamadas de saída por meio deste gateway de IP** .</span><span class="sxs-lookup"><span data-stu-id="fd841-159">If you use the Exchange Management Console, clear the **Allow outgoing calls through this IP gateway** check box.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="fd841-160">Se o seu plano de discagem de URI SIP SIP estiver associado a um único gateway IP, não permita chamadas de saída por meio desse gateway.</span><span class="sxs-lookup"><span data-stu-id="fd841-160">If your UM SIP URI dial plan is associated with only a single IP gateway, do not disallow outgoing calls through this gateway.</span></span>

    
    </div>

7.  <span data-ttu-id="fd841-161">Crie um atendedor automático da UM para cada plano de discagem do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fd841-161">Create a UM auto-attendant for each Lync Server dial plan.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="fd841-162">Não inclua espaços no nome do atendedor automático.</span><span class="sxs-lookup"><span data-stu-id="fd841-162">Do not include any spaces in the name of the auto attendant.</span></span>

    
    </div>
    
    ```powershell
    New-umautoattendant -name <auto attendant name> -umdialplan < name of dial plan created in step 1> -PilotIdentifierList <auto attendant phone number in E.164 format> -SpeechEnabled $true -Status Enabled
    ```
    <span data-ttu-id="fd841-163">Para obter detalhes, consulte:</span><span class="sxs-lookup"><span data-stu-id="fd841-163">For details, see:</span></span>
    
      - <span data-ttu-id="fd841-164">Para o Exchange 2007, consulte "New-UMAutoAttendant: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268689](https://go.microsoft.com/fwlink/p/?linkid=268689) .</span><span class="sxs-lookup"><span data-stu-id="fd841-164">For Exchange 2007, see "New-UMAutoAttendant: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268689](https://go.microsoft.com/fwlink/p/?linkid=268689).</span></span>
    
      - <span data-ttu-id="fd841-165">Para o Exchange 2010, consulte "New-UMAutoAttendant: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268690](https://go.microsoft.com/fwlink/p/?linkid=268690) .</span><span class="sxs-lookup"><span data-stu-id="fd841-165">For Exchange 2010, see "New-UMAutoAttendant: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268690](https://go.microsoft.com/fwlink/p/?linkid=268690).</span></span>
    
    <span data-ttu-id="fd841-166">A etapa a seguir deve ser realizada para cada usuário depois que você habilitar usuários do Lync Server para Enterprise Voice e conhecer seus URIs SIP.</span><span class="sxs-lookup"><span data-stu-id="fd841-166">The following step should be performed for each user after you have enabled Lync Server users for Enterprise Voice and know their SIP URIs.</span></span>

8.  <span data-ttu-id="fd841-167">Associe usuários do Exchange UM (cada um deve ser configurado com uma caixa Exchange mail) com o plano de discagem da UM e crie um URI SIP para cada usuário.</span><span class="sxs-lookup"><span data-stu-id="fd841-167">Associate Exchange UM users (each of whom should be configured with an Exchange mail box) with the UM dial plan and create a SIP URI for each user.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fd841-168">O <STRONG>SIPResourceIdentifier</STRONG> no exemplo a seguir deve ser o endereço SIP do usuário do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="fd841-168">The <STRONG>SIPResourceIdentifier</STRONG> in the following sample must be the SIP address of the Lync Server user.</span></span>

    
    </div>
    
    ```powershell
    enable-ummailbox -id <user name> -ummailboxpolicy <name of the mailbox policy for the dial plan created in step 1> -Extensions <extension> -SIPResourceIdentifier "<user name>@<full domain name>" -PIN <user pin>
    ```
    <span data-ttu-id="fd841-169">Para obter detalhes, consulte:</span><span class="sxs-lookup"><span data-stu-id="fd841-169">For details, see:</span></span>
    
      - <span data-ttu-id="fd841-170">Para o Exchange 2007, consulte "Enable-UMMailbox: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268691](https://go.microsoft.com/fwlink/p/?linkid=268691) .</span><span class="sxs-lookup"><span data-stu-id="fd841-170">For Exchange 2007, see "Enable-UMMailbox: Exchange 2007 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268691](https://go.microsoft.com/fwlink/p/?linkid=268691).</span></span>
    
      - <span data-ttu-id="fd841-171">Para o Exchange 2010, consulte "Enable-UMMailbox: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268692](https://go.microsoft.com/fwlink/p/?linkid=268692) .</span><span class="sxs-lookup"><span data-stu-id="fd841-171">For Exchange 2010, see "Enable-UMMailbox: Exchange 2010 Help" at [https://go.microsoft.com/fwlink/p/?LinkId=268692](https://go.microsoft.com/fwlink/p/?linkid=268692).</span></span>

<span data-ttu-id="fd841-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fd841-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

