---
title: 'Lync Server 2013: Criando ou modificando uma política de localização'
description: 'Lync Server 2013: Criando ou modificando uma política de localização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying a location policy
ms:assetid: 10338418-4da4-42df-b231-f52098c08dae
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687971(v=OCS.15)
ms:contentKeyID: 49733557
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba097ddb6e4ca8515c1eb33ae9d7e033821aef31
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431453"
---
# <a name="creating-or-modifying-a-location-policy-in-lync-server-2013"></a><span data-ttu-id="62b15-103">Criando ou modificando uma política de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62b15-103">Creating or modifying a location policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="62b15-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="62b15-104">

<span> </span></span></span>

<span data-ttu-id="62b15-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="62b15-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="62b15-106">No Lync Server 2013, você pode usar a política de localização para aplicar configurações relacionadas à funcionalidade Enhanced 9-1-1 (E9-1-1) e às configurações de localização para usuários ou contatos.</span><span class="sxs-lookup"><span data-stu-id="62b15-106">In Lync Server 2013, you can use the location policy to apply settings that relate to Enhanced 9-1-1 (E9-1-1) functionality and to location settings for users or contacts.</span></span> <span data-ttu-id="62b15-107">A política de localização determina se um usuário está habilitado para E9-1-1 e, em caso afirmativo, qual é o comportamento de uma chamada de emergência.</span><span class="sxs-lookup"><span data-stu-id="62b15-107">The location policy determines whether a user is enabled for E9-1-1, and if so what the behavior is of an emergency call.</span></span> <span data-ttu-id="62b15-108">Por exemplo, você pode usar a política de localização para definir qual número constitui uma chamada de emergência (por exemplo, 911 nos Estados Unidos), se a segurança corporativa deve ser notificada automaticamente e como a chamada deve ser roteada.</span><span class="sxs-lookup"><span data-stu-id="62b15-108">For example, you can use the location policy to define what number constitutes an emergency call (for example, 911 in the United States), whether corporate security should be automatically notified, and how the call should be routed.</span></span>

<span data-ttu-id="62b15-109">Você pode configurar as políticas de localização do grupo de **configuração de rede** no painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="62b15-109">You can configure location policies from the **Network Configuration** group in Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="62b15-110">No painel de controle do Lync Server, você pode exibir, criar, modificar ou excluir políticas de localização.</span><span class="sxs-lookup"><span data-stu-id="62b15-110">From Lync Server Control Panel you can view, create, modify, or delete location policies.</span></span> <span data-ttu-id="62b15-111">Use os procedimentos desta seção para criar ou modificar uma política de localização.</span><span class="sxs-lookup"><span data-stu-id="62b15-111">Use the procedures in this section to create or modify a location policy.</span></span> <span data-ttu-id="62b15-112">Para obter detalhes sobre a exclusão de políticas de localização, consulte [excluindo uma política de localização no Lync Server 2013](lync-server-2013-deleting-a-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="62b15-112">For details on deleting location policies, see [Deleting a location policy in Lync Server 2013](lync-server-2013-deleting-a-location-policy.md).</span></span>

<span data-ttu-id="62b15-113">No Lync Server 2013, você pode substituir a quantidade de tempo padrão entre solicitações do cliente para uma atualização de localização do serviço de informações de localização.</span><span class="sxs-lookup"><span data-stu-id="62b15-113">In Lync Server 2013, you can override the default amount of time between client requests for a location update from the Location Information service.</span></span> <span data-ttu-id="62b15-114">O valor padrão é de 4 horas.</span><span class="sxs-lookup"><span data-stu-id="62b15-114">The default value is 4 hours.</span></span> <span data-ttu-id="62b15-115">Use o cmdlet **set-CsLocationPolicy** com o parâmetro LocationRefreshInterval para substituir o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="62b15-115">Use the **Set-CsLocationPolicy** cmdlet with the LocationRefreshInterval parameter to override the default value.</span></span>

<div>

## <a name="to-create-a-new-location-policy-in-lync-server-control-panel"></a><span data-ttu-id="62b15-116">Para criar uma nova política de localização no painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="62b15-116">To create a new location policy in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="62b15-117">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="62b15-117">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="62b15-118">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62b15-118">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="62b15-119">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="62b15-119">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="62b15-120">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **política de localização**.</span><span class="sxs-lookup"><span data-stu-id="62b15-120">In the left navigation bar, click **Network Configuration** and then click **Location Policy**.</span></span>

4.  <span data-ttu-id="62b15-121">Na página **política de local** , clique em **novo** e selecione o tipo de política que você deseja criar:</span><span class="sxs-lookup"><span data-stu-id="62b15-121">On the **Location Policy** page, click **New** and then select the type of policy you want to create:</span></span>
    
      - <span data-ttu-id="62b15-122">Para criar uma política de site, clique em **política do site**.</span><span class="sxs-lookup"><span data-stu-id="62b15-122">To create a site policy, click **Site policy**.</span></span> <span data-ttu-id="62b15-123">Em **selecionar um site**, escolha o site ao qual você deseja aplicar a política e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="62b15-123">In **Select a Site**, choose the site to which you want the policy applied and click **OK**.</span></span> <span data-ttu-id="62b15-124">Na página **nova política de localização** , o **campo escopo** contém o valor **site** e o campo **nome** contém o nome do site que você escolheu.</span><span class="sxs-lookup"><span data-stu-id="62b15-124">On the **New Location Policy** page, the **Scope** field contains the value **Site**, and the **Name** field contains the name of the site you chose.</span></span> <span data-ttu-id="62b15-125">Não é possível modificar nenhum desses campos.</span><span class="sxs-lookup"><span data-stu-id="62b15-125">You cannot modify either of these fields.</span></span> <span data-ttu-id="62b15-126">Uma política de site é automaticamente aplicada a todos os usuários do site especificado e substitui a política global para esses usuários.</span><span class="sxs-lookup"><span data-stu-id="62b15-126">A site policy is automatically applied to all users on the specified site and overrides the global policy for those users.</span></span>
    
      - <span data-ttu-id="62b15-127">Para criar uma **política de usuário**, clique em **política de usuário**.</span><span class="sxs-lookup"><span data-stu-id="62b15-127">To create a **User policy**, click **User policy**.</span></span> <span data-ttu-id="62b15-128">Na **nova política de localização**, o campo **escopo** contém o valor **usuário**.</span><span class="sxs-lookup"><span data-stu-id="62b15-128">In the **New Location Policy**, the **Scope** field contains the value **User**.</span></span> <span data-ttu-id="62b15-129">Não é possível modificar esse valor.</span><span class="sxs-lookup"><span data-stu-id="62b15-129">You cannot modify this value.</span></span> <span data-ttu-id="62b15-130">No campo **nome** , digite o nome que você deseja dar a essa política.</span><span class="sxs-lookup"><span data-stu-id="62b15-130">In the **Name** field, type the name you want to give this policy.</span></span> <span data-ttu-id="62b15-131">Uma política de usuário não se aplica automaticamente a nenhum usuário.</span><span class="sxs-lookup"><span data-stu-id="62b15-131">A user policy does not automatically apply to any users.</span></span> <span data-ttu-id="62b15-132">Depois de criar a política de usuário, você deve conceder manualmente a política aos usuários ou sites de rede aos quais deseja aplicar a política.</span><span class="sxs-lookup"><span data-stu-id="62b15-132">After creating the user policy, you must manually grant the policy to the users or network sites to which you want to policy to apply.</span></span>

5.  <span data-ttu-id="62b15-133">Preencha os campos restantes da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="62b15-133">Fill in the remaining fields as follows:</span></span>
    
      - <span data-ttu-id="62b15-134">**Habilitar serviços de emergência aprimorados**   Marque esta caixa de seleção para habilitar os usuários associados a essa política para E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="62b15-134">**Enable enhanced emergency services**   Select this check box to enable the users associated with this policy for E9-1-1.</span></span> <span data-ttu-id="62b15-135">Quando os serviços de emergência estiverem habilitados, os clientes do Lync Server recuperarão informações de localização no registro e incluirão essas informações quando uma chamada de emergência for feita.</span><span class="sxs-lookup"><span data-stu-id="62b15-135">When emergency services are enabled, Lync Server clients will retrieve location information on registration and include that information when an emergency call is made.</span></span>
    
      - <span data-ttu-id="62b15-136">**Local**   Especifique um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="62b15-136">**Location**   Specify one of the following values:</span></span>
        
          - <span data-ttu-id="62b15-137">**Obrigatório**   O usuário será solicitado a inserir informações de localização quando o cliente se registrar em um novo local.</span><span class="sxs-lookup"><span data-stu-id="62b15-137">**Required**   The user will be prompted to input location information when the client registers at a new location.</span></span> <span data-ttu-id="62b15-138">O usuário pode ignorar a solicitação sem inserir informações.</span><span class="sxs-lookup"><span data-stu-id="62b15-138">The user can dismiss the prompt without entering any information.</span></span> <span data-ttu-id="62b15-139">Se as informações forem inseridas, uma chamada de emergência será atendida primeiramente pelo provedor de serviços de emergência para verificar o local antes de ser roteado para o operador de ponto de resposta de segurança pública (PSAP) (ou seja, o operador 911).</span><span class="sxs-lookup"><span data-stu-id="62b15-139">If information is entered, an emergency call will first be answered by the emergency services provider to verify the location before being routed to the Public Safety Answering Point (PSAP) operator (that is, the 911 operator).</span></span>
        
          - <span data-ttu-id="62b15-140">**Não é necessário**   O usuário não será solicitado a fornecer um local.</span><span class="sxs-lookup"><span data-stu-id="62b15-140">**Not Required**   The user will not be prompted for a location.</span></span> <span data-ttu-id="62b15-141">Quando uma chamada é feita sem informações de localização, o provedor de serviços de emergência atende a chamada e solicita um local.</span><span class="sxs-lookup"><span data-stu-id="62b15-141">When a call is made with no location information, the emergency services provider will answer the call and ask for a location.</span></span>
        
          - <span data-ttu-id="62b15-142">**Aviso**   Essa opção é a mesma **necessária** , exceto que o usuário não pode ignorar o prompt sem inserir informações de localização.</span><span class="sxs-lookup"><span data-stu-id="62b15-142">**Disclaimer**   This option is the same as **Required** except that the user cannot dismiss the prompt without entering location information.</span></span> <span data-ttu-id="62b15-143">O usuário ainda pode concluir uma chamada de emergência, mas nenhuma outra chamada pode ser completada sem inserir as informações.</span><span class="sxs-lookup"><span data-stu-id="62b15-143">The user can still complete an emergency call, but no other calls can be completed without entering the information.</span></span> <span data-ttu-id="62b15-144">Além disso, o texto de isenção de responsabilidade será exibido para o usuário que pode alertá-lo sobre as conseqüências de se recusar a inserir informações de localização.</span><span class="sxs-lookup"><span data-stu-id="62b15-144">In addition, disclaimer text will be displayed to the user that can alert them to the consequences of declining to enter location information.</span></span> <span data-ttu-id="62b15-145">Para definir o texto de isenção de responsabilidade, você deve usar o Shell de gerenciamento do Lync Server para executar o cmdlet **set-CsLocationPolicy** ou o cmdlet **New-CsLocationPolicy** com o parâmetro EnhancedEmergencyServiceDisclaimer.</span><span class="sxs-lookup"><span data-stu-id="62b15-145">To set the disclaimer text, you must use Lync Server Management Shell to run the **Set-CsLocationPolicy** cmdlet or the **New-CsLocationPolicy** cmdlet with the EnhancedEmergencyServiceDisclaimer parameter.</span></span> <span data-ttu-id="62b15-146">Para obter detalhes, consulte [set-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsLocationPolicy) ou [New-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsLocationPolicy) na documentação do Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62b15-146">For details, see [Set-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsLocationPolicy) or [New-CsLocationPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsLocationPolicy) in the Lync Server Management Shell documentation.</span></span>
            
            <div>
            

            > [!NOTE]  
            > <span data-ttu-id="62b15-147">No Lync Server 2013, você pode usar a política de localização para definir diferentes isenções para locais diferentes ou conjuntos de usuários diferentes, ao contrário do Lync Server 2010, onde você pode especificar apenas um aviso global para toda a organização.</span><span class="sxs-lookup"><span data-stu-id="62b15-147">In Lync Server 2013, you can use location policy to set different disclaimers for different locales or different sets of users, unlike in Lync Server 2010 where you could specify only a global disclaimer for the entire organization.</span></span>

            
            </div>
    
      - <span data-ttu-id="62b15-148">**Usar local somente para serviços de emergência**   O Lync pode usar as informações de localização por vários motivos (por exemplo, para notificar os colegas de sua localização atual).</span><span class="sxs-lookup"><span data-stu-id="62b15-148">**Use location for emergency services only**   Lync can use location information for various reasons (for example, to notify teammates of your current location).</span></span> <span data-ttu-id="62b15-149">Marque esta caixa de seleção para garantir que as informações de localização estejam disponíveis somente para uso com uma chamada de emergência.</span><span class="sxs-lookup"><span data-stu-id="62b15-149">Select this check box to ensure location information is available only for use with an emergency call.</span></span>
    
      - <span data-ttu-id="62b15-150">**Uso de PSTN**   O uso da rede telefônica pública comutada (PSTN) que será usado para determinar qual rota de voz será usada para direcionar as chamadas de emergência dos clientes que usam esse perfil.</span><span class="sxs-lookup"><span data-stu-id="62b15-150">**PSTN usage**   The public switched telephone network (PSTN) usage that will be used to determine which voice route will be used to route emergency calls from clients using this profile.</span></span> <span data-ttu-id="62b15-151">A rota associada a esse uso deve apontar para um tronco SIP dedicado a chamadas de emergência ou a um gateway de Emergency Location Identification Number (ELIN) que encaminha as chamadas de emergência ao Public Safety Answering Point (PSAP) mais próximo.</span><span class="sxs-lookup"><span data-stu-id="62b15-151">The route associated with this usage should point to a SIP trunk dedicated to emergency calls or to an Emergency Location Identification Number (ELIN) gateway that routes emergency calls to the nearest Public Safety Answering Point (PSAP).</span></span>
    
      - <span data-ttu-id="62b15-152">**Número de discagem de emergência**   O número discado para acessar serviços de emergência.</span><span class="sxs-lookup"><span data-stu-id="62b15-152">**Emergency dial number**   The number that is dialed to reach emergency services.</span></span> <span data-ttu-id="62b15-153">Nos Estados Unidos, esse valor é 911.</span><span class="sxs-lookup"><span data-stu-id="62b15-153">In the United States this value is 911.</span></span> <span data-ttu-id="62b15-154">A cadeia de caracteres deve ser feita dos dígitos de 0 a 9 e pode ter de 1 a 10 dígitos.</span><span class="sxs-lookup"><span data-stu-id="62b15-154">The string must be made of the digits 0 through 9 and can be from 1 to 10 digits in length.</span></span>
    
      - <span data-ttu-id="62b15-155">**Máscara de discagem de emergência**   Um número que você deseja traduzir para o valor do valor do número de discagem de emergência quando ele for discado.</span><span class="sxs-lookup"><span data-stu-id="62b15-155">**Emergency dial mask**   A number that you want to translate into the value of the emergency dial number value when it is dialed.</span></span> <span data-ttu-id="62b15-156">Por exemplo, se você inserir um valor de 212 nesse campo e o campo de número de discagem de emergência tiver um valor de 911, se um usuário discar 212, a chamada será feita a 911.</span><span class="sxs-lookup"><span data-stu-id="62b15-156">For example, if you enter a value of 212 in this field and the emergency dial number field has a value of 911, if a user dials 212 the call will be made to 911.</span></span> <span data-ttu-id="62b15-157">Isso permite a discagem de números de emergência alternativos e ainda assim acessar os serviços de emergência (por exemplo, se alguém de um país ou região com um número de emergência diferente tenta discar o número desse país ou região em vez do número para o país ou região atual).</span><span class="sxs-lookup"><span data-stu-id="62b15-157">This allows for alternate emergency numbers to be dialed and still have the call reach emergency services (for example, if someone from a country or region with a different emergency number attempts to dial that country or region’s number rather than the number for the country or region they are currently in).</span></span> <span data-ttu-id="62b15-158">É possível definir várias máscaras de discagem de emergência separando os valores com ponto e vírgulas.</span><span class="sxs-lookup"><span data-stu-id="62b15-158">You can define multiple emergency dial masks by separating the values with semicolons.</span></span> <span data-ttu-id="62b15-159">Por exemplo, 212;414.</span><span class="sxs-lookup"><span data-stu-id="62b15-159">For example, 212;414.</span></span> <span data-ttu-id="62b15-160">O comprimento máximo da cadeia é de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="62b15-160">Maximum length of the string is 100 characters.</span></span> <span data-ttu-id="62b15-161">Cada caractere precisa ser um dígito de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="62b15-161">Each character must be a digit 0 through 9.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="62b15-162">Certifique-se de que o valor de máscara de discagem especificado não seja igual a um número em um intervalo de linha de estacionamento de chamada.</span><span class="sxs-lookup"><span data-stu-id="62b15-162">Ensure that the specified dial mask value is not the same as a number in a call park orbit range.</span></span> <span data-ttu-id="62b15-163">O roteamento do parque de chamadas terá precedência com a conversão de cadeia de discagem de emergência.</span><span class="sxs-lookup"><span data-stu-id="62b15-163">Call park routing will take precedence over emergency dial string conversion.</span></span> <span data-ttu-id="62b15-164">Para ver os intervalos de o parque de chamadas existentes, clique em <STRONG>recursos de voz</STRONG> na barra de navegação à esquerda e clique em <STRONG>ligar para estacionamento</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="62b15-164">To see the existing call park orbit ranges, click <STRONG>Voice Features</STRONG> in the left navigation bar and then click <STRONG>Call Park</STRONG>.</span></span> <span data-ttu-id="62b15-165">Para obter detalhes, consulte <A href="lync-server-2013-configure-phone-number-extensions-for-parking-calls.md">Configurar extensões de número de telefone para chamadas de estacionamento no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="62b15-165">For details, see <A href="lync-server-2013-configure-phone-number-extensions-for-parking-calls.md">Configure phone number extensions for parking calls in Lync Server 2013</A>.</span></span>

        
        </div>
    
      - <span data-ttu-id="62b15-166">**URI de notificação**   Um ou mais URIs (Uniform Resource Identifiers) SIP para serem notificados quando uma chamada de emergência for feita.</span><span class="sxs-lookup"><span data-stu-id="62b15-166">**Notification URI**   One or more SIP Uniform Resource Identifiers (URIs) to be notified when an emergency call is made.</span></span> <span data-ttu-id="62b15-167">Por exemplo, o escritório de segurança da empresa pode ser notificado por uma mensagem instantânea sempre que uma chamada de emergência é feita.</span><span class="sxs-lookup"><span data-stu-id="62b15-167">For example, the company security office could be notified through an instant message whenever an emergency call is made.</span></span> <span data-ttu-id="62b15-168">Se a localização do chamador estiver disponível, essa localização será incluída na notificação.</span><span class="sxs-lookup"><span data-stu-id="62b15-168">If the caller’s location is available that location will be included in the notification.</span></span> <span data-ttu-id="62b15-169">Vários URIs SIP podem ser incluídos como uma lista separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="62b15-169">Multiple SIP URIs can be included as a comma-separated list.</span></span> <span data-ttu-id="62b15-170">Por exemplo, "sip:security@litwareinc.com","sip:kmyer@litwareinc.com".</span><span class="sxs-lookup"><span data-stu-id="62b15-170">For example, "sip:security@litwareinc.com","sip:kmyer@litwareinc.com".</span></span> <span data-ttu-id="62b15-171">As listas de distribuição são aceitas.</span><span class="sxs-lookup"><span data-stu-id="62b15-171">Distribution lists are supported.</span></span> <span data-ttu-id="62b15-172">A cadeia de cadeia de caracteres precisa ter de 1 a 256 caracteres e precisa começar com o prefixo "sip:".</span><span class="sxs-lookup"><span data-stu-id="62b15-172">The string must be from 1 to 256 characters in length and must begin with the prefix "sip:".</span></span> <span data-ttu-id="62b15-173">Antes de clicar no campo URI da notificação, um exemplo é exibido.</span><span class="sxs-lookup"><span data-stu-id="62b15-173">Before you click in the Notification URI field an example is displayed.</span></span>
    
      - <span data-ttu-id="62b15-174">**URL de conferência**   O URI SIP, nesse caso, o número de telefone, de terceiros que serão emessados em todas as chamadas de emergência feitas.</span><span class="sxs-lookup"><span data-stu-id="62b15-174">**Conference URI**   The SIP URI, in this case the telephone number, of a third party that will be conferenced in to any emergency calls that are made.</span></span> <span data-ttu-id="62b15-175">Por exemplo, o Office de segurança da empresa pode receber uma chamada quando uma chamada de emergência é feita e ouvir ou participar dessa chamada (dependendo do valor fornecido no campo **modo de conferência** ).</span><span class="sxs-lookup"><span data-stu-id="62b15-175">For example, the company security office could receive a call when an emergency call is made and listen in or participate in that call (depending on the value supplied in the **Conference mode** field).</span></span> <span data-ttu-id="62b15-176">A cadeia de caracteres precisa ter de 1 a 256 caracteres e precisa começar com o prefixo sip:.</span><span class="sxs-lookup"><span data-stu-id="62b15-176">The string must be from 1 to 256 characters in length and must begin with the prefix sip:.</span></span> <span data-ttu-id="62b15-177">Um exemplo é exibido até que você clique dentro desse campo.</span><span class="sxs-lookup"><span data-stu-id="62b15-177">An example is displayed until you click inside this field.</span></span>
    
      - <span data-ttu-id="62b15-178">**Modo de conferência**   Se você especificar um valor no campo **URI da conferência** , o **modo de conferência** determinará se uma terceira parte pode participar da chamada ou somente pode ouvi-la.</span><span class="sxs-lookup"><span data-stu-id="62b15-178">**Conference mode**   If you specify a value in the **Conference URI** field, the **Conference mode** determines whether a third party can participate in the call or can only listen in.</span></span> <span data-ttu-id="62b15-179">Especifique uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="62b15-179">Specify one of the following options:</span></span>
        
          - <span data-ttu-id="62b15-180">**Unilateral**   Uma terceira parte só pode ouvir a conversa entre o chamador e o operador PSAP.</span><span class="sxs-lookup"><span data-stu-id="62b15-180">**One-way**   A third party can only listen to the conversation between the caller and the PSAP operator.</span></span>
        
          - <span data-ttu-id="62b15-181">**Bidirecional**   Uma terceira parte pode ouvir e participar da chamada entre o chamador e o operador PSAP.</span><span class="sxs-lookup"><span data-stu-id="62b15-181">**Two-way**   A third party can listen in and participate in the call between the caller and the PSAP operator.</span></span>

6.  <span data-ttu-id="62b15-182">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="62b15-182">Click **Commit**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="62b15-183">Quando você cria uma política de usuário, inicialmente essa política não se aplica a nenhum usuário ou site de rede.</span><span class="sxs-lookup"><span data-stu-id="62b15-183">When you create a user policy, initially that policy does not apply to any users or network sites.</span></span> <span data-ttu-id="62b15-184">Para aplicar a política a um usuário, clique em <STRONG>usuários</STRONG> na barra de navegação à esquerda.</span><span class="sxs-lookup"><span data-stu-id="62b15-184">To apply the policy to a user, click <STRONG>Users</STRONG> in the left navigation bar.</span></span> <span data-ttu-id="62b15-185">Localize o usuário ao qual você deseja aplicar a política.</span><span class="sxs-lookup"><span data-stu-id="62b15-185">Find the user to which you want to apply the policy.</span></span> <span data-ttu-id="62b15-186">No menu <STRONG>Editar</STRONG>, clique em <STRONG>Exibir detalhes</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="62b15-186">On the <STRONG>Edit</STRONG> menu, click <STRONG>Show details</STRONG>.</span></span> <span data-ttu-id="62b15-187">Na página <STRONG>Editar usuário do Lync Server</STRONG> , selecione a lista de novos locais na lista suspensa <STRONG>política de localização</STRONG> e clique em <STRONG>confirmar</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="62b15-187">On the <STRONG>Edit Lync Server User</STRONG> page, select the new location policy from the <STRONG>Location policy</STRONG> drop-down list and then click <STRONG>Commit</STRONG>.</span></span><BR><span data-ttu-id="62b15-188">Para aplicar a política a um site de rede, clique em <STRONG>configuração de rede</STRONG> na barra de navegação à esquerda e, em seguida, clique em <STRONG>site</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="62b15-188">To apply the policy to a network site, click <STRONG>Network Configuration</STRONG> in the left navigation bar and then click <STRONG>Site</STRONG>.</span></span> <span data-ttu-id="62b15-189">Localize o site de rede ao qual você deseja aplicar a política.</span><span class="sxs-lookup"><span data-stu-id="62b15-189">Find the network site to which you want to apply the policy.</span></span> <span data-ttu-id="62b15-190">No menu <STRONG>Editar</STRONG>, clique em <STRONG>Exibir detalhes</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="62b15-190">On the <STRONG>Edit</STRONG> menu, click <STRONG>Show details</STRONG>.</span></span> <span data-ttu-id="62b15-191">Em <STRONG>Editar site</STRONG>, selecione a nova política de localização na lista suspensa <STRONG>diretiva de local</STRONG> e clique em <STRONG>confirmar</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="62b15-191">In <STRONG>Edit Site</STRONG>, select the new location policy from the <STRONG>Location policy</STRONG> drop-down list and then click <STRONG>Commit</STRONG>.</span></span>

    
    </div>

</div>

<div>

## <a name="to-modify-a-location-policy-in-lync-server-control-panel"></a><span data-ttu-id="62b15-192">Para modificar uma política de localização no painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="62b15-192">To modify a location policy in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="62b15-193">Usando uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes), ou está atribuída à função CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="62b15-193">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="62b15-194">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="62b15-194">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="62b15-195">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="62b15-195">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="62b15-196">Na barra de navegação à esquerda, clique em **configuração de rede** e, em seguida, clique em **política de localização**.</span><span class="sxs-lookup"><span data-stu-id="62b15-196">In the left navigation bar, click **Network Configuration** and then click **Location Policy**.</span></span>

4.  <span data-ttu-id="62b15-197">Na página **política de localização** , selecione a política de localização que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="62b15-197">On the **Location Policy** page, select the location policy that you want to modify.</span></span>

5.  <span data-ttu-id="62b15-198">No menu **Editar**, clique em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="62b15-198">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="62b15-199">Na página **Editar política de local** , modifique os campos conforme necessário (para obter detalhes, veja a etapa 5 nos procedimentos "para criar uma nova política de local" anteriormente neste tópico).</span><span class="sxs-lookup"><span data-stu-id="62b15-199">On the **Edit Location Policy** page, modify the fields as necessary (for details, see Step 5 in the "To create a new location policy" procedures earlier in this topic).</span></span>

7.  <span data-ttu-id="62b15-200">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="62b15-200">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="62b15-201">Confira também</span><span class="sxs-lookup"><span data-stu-id="62b15-201">See Also</span></span>


[<span data-ttu-id="62b15-202">Excluindo uma política de localização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62b15-202">Deleting a location policy in Lync Server 2013</span></span>](lync-server-2013-deleting-a-location-policy.md)  


[<span data-ttu-id="62b15-203">Definindo a política de localização do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62b15-203">Defining the location policy for Lync Server 2013</span></span>](lync-server-2013-defining-the-location-policy.md)  


[<span data-ttu-id="62b15-204">Configurar extensões de número de telefone para chamadas com estacionamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="62b15-204">Configure phone number extensions for parking calls in Lync Server 2013</span></span>](lync-server-2013-configure-phone-number-extensions-for-parking-calls.md)  
  

<span data-ttu-id="62b15-205"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="62b15-205"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

