---
title: 'Lync Server 2013: criar ou modificar um fluxo de trabalho de grupo coletivo'
description: 'Lync Server 2013: crie ou modifique um fluxo de trabalho de grupo coletivo.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a hunt group workflow
ms:assetid: dcb9effb-5d12-4dee-80fc-ab9654222d5a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205321(v=OCS.15)
ms:contentKeyID: 48185596
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95f6374352c87d13b1e5c09bcef267059016eae0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431831"
---
# <a name="create-or-modify-a-hunt-group-workflow-in-lync-server-2013"></a><span data-ttu-id="1cc50-103">Criar ou modificar um fluxo de trabalho de grupo coletivo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cc50-103">Create or modify a hunt group workflow in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1cc50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1cc50-104">

<span> </span></span></span>

<span data-ttu-id="1cc50-105">_**Tópico da última modificação:** 2013-09-11_</span><span class="sxs-lookup"><span data-stu-id="1cc50-105">_**Topic Last Modified:** 2013-09-11_</span></span>

<span data-ttu-id="1cc50-106">Use um dos procedimentos a seguir para criar ou modificar um fluxo de trabalho de grupo coletivo.</span><span class="sxs-lookup"><span data-stu-id="1cc50-106">Use one of the following procedures to create or modify a hunt group workflow.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1cc50-107">Você pode usar o Shell de gerenciamento do Lync Server ou a ferramenta de configuração de grupo de resposta para criar e modificar fluxos de trabalho de grupo de busca.</span><span class="sxs-lookup"><span data-stu-id="1cc50-107">You can use Lync Server Management Shell or the Response Group Configuration Tool to create and modify hunt group workflows.</span></span> <span data-ttu-id="1cc50-108">Você pode acessar a ferramenta de configuração do grupo de resposta no painel de controle do Lync Server ou abrindo a página da Web diretamente de um navegador da Web, digitando a seguinte URL: <STRONG>https://</STRONG> &lt; webPoolFqdn &gt; <STRONG>/RgsConfig</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-108">You can access the Response Group Configuration Tool from Lync Server Control Panel, or by opening the webpage directly from a web browser by typing the following URL: <STRONG>https://</STRONG>&lt;webPoolFqdn&gt;<STRONG>/RgsConfig</STRONG>.</span></span>



</div>

<div>

## <a name="to-use-response-group-configuration-tool-to-create-or-modify-a-hunt-group-workflow"></a><span data-ttu-id="1cc50-109">Para usar a ferramenta de configuração de grupo de resposta para criar ou modificar um fluxo de trabalho de grupo coletivo</span><span class="sxs-lookup"><span data-stu-id="1cc50-109">To use Response Group Configuration Tool to create or modify a hunt group workflow</span></span>

1.  <span data-ttu-id="1cc50-110">Faça logon como um membro do grupo RTCUniversalServerAdmins ou como um membro de uma das funções administrativas predefinidas que oferecem suporte ao Grupo de Resposta.</span><span class="sxs-lookup"><span data-stu-id="1cc50-110">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="1cc50-111">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="1cc50-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="1cc50-112">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="1cc50-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="1cc50-113">Na barra de navegação à esquerda, clique em **Grupos de Resposta** e em **Fluxo de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-113">In the left navigation bar, click **Response Groups**, and then click **Workflow**.</span></span>

4.  <span data-ttu-id="1cc50-114">Na página **Fluxo de Trabalho**, clique em **Criar ou editar um fluxo de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-114">On the **Workflow** page, click **Create or edit a workflow**.</span></span>

5.  <span data-ttu-id="1cc50-115">No campo de pesquisa **Selecione um Serviço**, digite parte ou todo o nome do serviço do **ApplicationServer** que hospeda o fluxo de trabalho que você deseja alterar ou criar.</span><span class="sxs-lookup"><span data-stu-id="1cc50-115">In the **Select a Service** search field, type all or part of the name of the **ApplicationServer** service that hosts the workflow that you want to create or change.</span></span> <span data-ttu-id="1cc50-116">Na lista resultante de serviços, clique no serviço que você deseja e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-116">In the resulting list of services, click the service that you want, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-117">A ferramenta de configuração de grupo de resposta é aberta.</span><span class="sxs-lookup"><span data-stu-id="1cc50-117">The Response Group Configuration Tool opens.</span></span> <span data-ttu-id="1cc50-118">Você também pode abrir a ferramenta de configuração de grupo de resposta diretamente de um navegador da Web digitando a seguinte URL: <STRONG>https://</STRONG> &lt; webPoolFqdn &gt; <STRONG>/RgsConfig</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-118">You can also open the Response Group Configuration Tool directly from a web browser by typing the following URL: <STRONG>https://</STRONG>&lt;webPoolFqdn&gt;<STRONG>/RgsConfig</STRONG>.</span></span>

    
    </div>

6.  <span data-ttu-id="1cc50-119">Siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="1cc50-119">Do one of the following:</span></span>
    
      - <span data-ttu-id="1cc50-120">Em **Criar um Novo Fluxo de Trabalho**, próximo ao **Grupo de busca, clique em Criar**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-120">Under **Create a New Workflow**, next to **Hunt Group, click Create**.</span></span>
    
      - <span data-ttu-id="1cc50-121">Em **Gerenciar um Fluxo de Trabalho Existente**, localize o fluxo de trabalho que você deseja alterar e, em **Ação**, clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-121">Under **Manage an Existing Workflow**, locate the workflow you want to change, and then under **Action**, click **Edit**.</span></span>

7.  <span data-ttu-id="1cc50-122">Se estiver pronto para que os usuários comecem a fazer chamadas para o fluxo de trabalho, selecione **Ativar o fluxo de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-122">If you are ready for users to start calling the workflow, select **Activate the workflow**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-p105">Se você estiver criando um fluxo de trabalho gerenciado, é necessário selecionar <STRONG>Ativar o fluxo de trabalho</STRONG>. Após salvar o fluxo de trabalho gerenciado ativo, é possível modificar e desativá-lo.</span><span class="sxs-lookup"><span data-stu-id="1cc50-p105">If you are to creating a managed workflow, you need to select <STRONG>Activate the workflow</STRONG>. After you save the active, managed workflow, you can then modify and deactivate it.</span></span>

    
    </div>

8.  <span data-ttu-id="1cc50-125">Para permitir que usuários federados façam chamadas para o grupo, selecione a opção **Habilitar para federação**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-125">To allow federated users to call the group, select the **Enable for federation** check box.</span></span> <span data-ttu-id="1cc50-126">Você também deve ter uma política de acesso externo que se aplica ao aplicativo de grupo de resposta configurado para Federação.</span><span class="sxs-lookup"><span data-stu-id="1cc50-126">You must also have an external access policy that applies to the Response Group application configured for federation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-127">A política de acesso externo global global aplica-se ao aplicativo de grupo de resposta.</span><span class="sxs-lookup"><span data-stu-id="1cc50-127">The global external access policy applies to the Response Group application.</span></span> <span data-ttu-id="1cc50-128">Você pode configurar a política global para a Federação de grupo de resposta usando o painel de controle do Lync Server ou usando o cmdlet <STRONG>set-CsExternalAccessPolicy</STRONG> para definir o parâmetro EnableOutsideAccess como true.</span><span class="sxs-lookup"><span data-stu-id="1cc50-128">You can configure the global policy for response group federation by using Lync Server Control Panel or by using the <STRONG>Set-CsExternalAccessPolicy</STRONG> cmdlet to set the EnableOutsideAccess parameter to True.</span></span> <span data-ttu-id="1cc50-129">Lembre-se que as configurações de política global se aplicam a todos os usuários, a não ser que eles sejam atribuídos com uma política de usuário ou de site.</span><span class="sxs-lookup"><span data-stu-id="1cc50-129">Keep in mind that global policy settings apply to all users unless they are assigned a site or user policy.</span></span> <span data-ttu-id="1cc50-130">Portanto, antes de alterar esta configuração para grupos de resposta, certifique-se de que as configurações de federação cumpre os requisitos da sua organização.</span><span class="sxs-lookup"><span data-stu-id="1cc50-130">Therefore, before changing this setting for response groups, make sure that the federation setting meets the requirements of your organization.</span></span> <span data-ttu-id="1cc50-131">Para obter detalhes sobre como as políticas se aplicam aos usuários, consulte <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">gerenciar a política de acesso externo no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-131">For details about how policies apply to users, see <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">Manage external access policy in Lync Server 2013</A>.</span></span> <span data-ttu-id="1cc50-132">Para obter detalhes sobre a configuração de Federação, consulte <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsExternalAccessPolicy">set-CsExternalAccessPolicy</A>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-132">For details about the federation setting, see <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsExternalAccessPolicy">Set-CsExternalAccessPolicy</A>.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-133">Os usuários hospedados no Lync Online não podem fazer chamadas para grupos de resposta hospedados em uma implantação local.</span><span class="sxs-lookup"><span data-stu-id="1cc50-133">Users who are hosted in Lync Online can’t place calls to response groups that are hosted in an on-premise deployment.</span></span> <span data-ttu-id="1cc50-134">Isso é verdade nas implantações híbridas e nos casos em que uma implantação local é federada com uma implantação do Lync Online.</span><span class="sxs-lookup"><span data-stu-id="1cc50-134">This is true in both hybrid deployments and in cases where an on-premise deployment is federated with a Lync Online deployment.</span></span>

    
    </div>

9.  <span data-ttu-id="1cc50-135">Para ocultar a identidade de operadores durante as chamadas, selecione a opção **Habilitar anonimato do operador**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-135">To hide the identity of agents during calls, select the **Enable agent anonymity** check box.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-p109">Chamadas anônimas não podem ter início com sistemas de mensagens instantâneas (IM) ou vídeo, embora o operador ou chamadas possam adicionar IM e vídeo depois que a chamada estiver estabelecida. Um operador anônimo também pode colocar chamadas em espera, transferir (transferências ocultas e de consulta), estacionar e recuperar chamadas. Chamadas anônimas não oferecem suporte a conferência, compartilhamento de aplicativos, transferência de arquivos, whiteboarding e colaboração de dados e gravação de chamadas. Agentes utilizando o Plugin Lync VDI podem atender chamadas em entrada anonimamente, mas não podem realizar chamadas em saída anonimamente.</span><span class="sxs-lookup"><span data-stu-id="1cc50-p109">Anonymous calls cannot start with instant messaging (IM) or video, although the agent or the caller can add IM and video after the call is established. An anonymous agent can also put calls on hold, transfer calls (both blind and consultative transfers), and park and retrieve calls. Anonymous calls do not support conferencing, application sharing and desktop sharing, file transfer, whiteboarding and data collaboration, and call recording. Agents using the Lync VDI Plugin can receive incoming calls anonymously, but they cannot make outgoing calls anonymously.</span></span>

    
    </div>

10. <span data-ttu-id="1cc50-140">Sob **Insira o endereço do grupo que receberá as chamadas**, digite o endereço URI SIP primário do grupo que irá receber chamadas para o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1cc50-140">Under **Enter the address of the group that will receive the calls**, type the primary SIP uniform resource identifier (URI) address of the group that will answer calls to the workflow.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-141">O URI primário para um fluxo de trabalho é como o fluxo de trabalho é identificado e referenciado.</span><span class="sxs-lookup"><span data-stu-id="1cc50-141">The primary URI for a workflow is how the workflow is identified and referenced.</span></span> <span data-ttu-id="1cc50-142">O URI SIP que você insere é criado como um objeto de contato nos serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1cc50-142">The SIP URI that you enter is created as a contact object in Active Directory Domain Services.</span></span> <span data-ttu-id="1cc50-143">Para criar o URI, o objeto deve ser exclusivo no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1cc50-143">To create the URI, the object must be unique in Active Directory.</span></span>

    
    </div>

11. <span data-ttu-id="1cc50-144">Em **nome para exibição**, digite o nome que você deseja exibir para o fluxo de trabalho (por exemplo, grupo de resposta de vendas).</span><span class="sxs-lookup"><span data-stu-id="1cc50-144">In **Display name**, type the name that you want to display for the workflow (for example, Sales Response Group).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-145">Não inclua os caracteres " &lt; " ou " &gt; " no nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="1cc50-145">Do not include the "&lt;" or "&gt;" characters in the display name.</span></span> <span data-ttu-id="1cc50-146">Não use os nomes de exibição a seguir, pois são reservados: <STRONG>Observador de Presença RG</STRONG> ou <STRONG>Serviço de Anúncio</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-146">Do not use the following display names because they are reserved: <STRONG>RGS Presence Watcher</STRONG> or <STRONG>Announcement Service</STRONG>.</span></span>

    
    </div>

12. <span data-ttu-id="1cc50-147">Sob **Número de telefone**, digite o URI de linha para o grupo de resposta (por exemplo, +14255550165).</span><span class="sxs-lookup"><span data-stu-id="1cc50-147">Under **Telephone number**, type the line URI for the response group (for example, +14255550165).</span></span>

13. <span data-ttu-id="1cc50-148">Em **Número de Exibição**, digite o número conforme deseja que apareça para o grupo de resposta (por exemplo, +1 (425) 555-0165).</span><span class="sxs-lookup"><span data-stu-id="1cc50-148">In **Display number**, type the number as you want it to appear for the response group (for example, +1 (425) 555-0165).</span></span>

14. <span data-ttu-id="1cc50-149">Adicionais Em **Descrição**, digite uma descrição para o fluxo de trabalho como deseja que ele apareça no cartão de visita do cliente do Lync.</span><span class="sxs-lookup"><span data-stu-id="1cc50-149">(Optional) In **Description**, type a description for the workflow as you want it to appear on the contact card in Lync client.</span></span>

15. <span data-ttu-id="1cc50-150">Em **Tipo de fluxo de trabalho**, selecione **Gerenciado** se este fluxo de trabalho será gerenciado por um Gerente o Grupo de Resposta.</span><span class="sxs-lookup"><span data-stu-id="1cc50-150">In **Workflow Type**, select **Managed** if this workflow will be managed by a Response Group Manager.</span></span> <span data-ttu-id="1cc50-151">Siga este procedimento para atribuir gerentes de grupo de resposta ao fluxo de trabalho:</span><span class="sxs-lookup"><span data-stu-id="1cc50-151">Do the following to assign Response Group Managers to the workflow:</span></span>
    
    1.  <span data-ttu-id="1cc50-152">Digite o URI SIP de um gerente para este fluxo de trabalho e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-152">Type the SIP URI of a manager for this workflow, and click **Add**.</span></span>
    
    2.  <span data-ttu-id="1cc50-153">Digite o URI SIP de gerentes adicionais para adicionar ao fluxo de trabalho e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-153">Type the SIP URI of additional managers to add to the workflow, and click **Add**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="1cc50-p113">Cada usuário que é designado como um gerente de um grupo de resposta deve ser atribuído à função CsResponseGroupManager. Se os usuários não sã atribuídos com esta função, eles não podem gerenciar grupos de resposta.</span><span class="sxs-lookup"><span data-stu-id="1cc50-p113">Every user who is designated as a manager of a response group must be assigned the CsResponseGroupManager role. If users are not assigned this role, they cannot manage response groups.</span></span>

    
    </div>

16. <span data-ttu-id="1cc50-156">Sob **Etapa 2 Selecione um Idioma**, clique no idioma que deseja usar para reconhecimento de fala e conversão de texto em fala.</span><span class="sxs-lookup"><span data-stu-id="1cc50-156">Under **Step 2 Select a Language**, click the language that you want to use for speech recognition and text-to-speech.</span></span>

17. <span data-ttu-id="1cc50-157">Se você deseja configurar uma mensagem de boas vindas, sob **Etapa 3 Configure uma Mensagem de Boas Vindas**, selecione a opção **Reproduzir uma mensagem de boas vindas** e execute um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="1cc50-157">If you want to configure a welcome message, under **Step 3 Configure a Welcome Message**, select the **Play a welcome message** check box, and then do one of the following:</span></span>
    
      - <span data-ttu-id="1cc50-158">Para inserir uma mensagem de boas vindas como texto convertido para fala para os chamadores, clique em **Usar conversão de texto em fala** e digite a mensagem de boas vindas na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="1cc50-158">To enter the welcome message as text that is converted to speech for callers, click **Use text-to-speech**, and then type the welcome message in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1cc50-p114">Não inclua tags HTML no texto digitado. Se você incluir tags HTML, receberá uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="1cc50-p114">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
    
      - <span data-ttu-id="1cc50-p115">Para usar uma gravação de arquivo de áudio wave (.wav) ou (.wma) do Windows Media para a mensagem de boas vindas, clique em **Selecionar uma gravação**. Se você deseja carregar um novo arquivo de áudio, clique no link **uma gravação**. Na janela do navegador, clique em **Procurar**, selecione o arquivo de áudio que deseja usar e clique em **Abrir**. Clique em **Carregar** para carregar o arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="1cc50-p115">To use a wave (.wav) or Windows Media audio (.wma) file recording for the welcome message, click **Select a recording**. If you want to upload a new audio file, click the **a recording** link. In the new browser window, click **Browse**, select the audio file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1cc50-165">Todos os arquivos de áudio fornecidos pelo usuário devem estar de acordo com determinados requisitos.</span><span class="sxs-lookup"><span data-stu-id="1cc50-165">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="1cc50-166">Para obter detalhes sobre os formatos de arquivo com suporte, consulte <A href="lync-server-2013-technical-requirements-for-response-group.md">requisitos técnicos para o grupo de resposta no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-166">For details about supported file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

18. <span data-ttu-id="1cc50-167">Sob **Etapa 4 Especifique seu Horário Comercial**, em **Seu fuso horário**, clique no fuso horário para o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1cc50-167">Under **Step 4 Specify Your Business Hours**, in **Your time zone**, click the time zone for the workflow.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-p117">O fuso horário é onde os chamadores e operadores do fluxo de trabalho residem. Ele é usado para calcular os horários de abertura e encerramento. Por exemplo, se o fluxo de trabalho está configurado para usar o fuso horário da costa leste norte-americana e o fluxo de trabalho estiver agendado para abrir às 7:00 A.M e fechar às 11:00 P.M., os horários de abertura e fechamento são assumidos como sendo 7:00 horário da costa leste e 23:00 horário da costa leste, respectivamente (você deve inserir os horários na notação de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="1cc50-p117">The time zone is the time zone where the callers and agents of the workflow reside. It is used to calculate the open and close hours. For example, if the workflow is configured to use the North American Eastern Time zone and the workflow is scheduled to open at 7:00 A.M. and close at 11:00 P.M., the open and close times are assumed to be 7:00 Eastern Time and 23:00 Eastern Time respectively. (You must enter the times in 24-hour time notation.)</span></span>

    
    </div>

19. <span data-ttu-id="1cc50-173">Selecione o tipo de agenda de horário comercial que deseja usar executando um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="1cc50-173">Select the type of business hours schedule you want to use by doing one of the following:</span></span>
    
      - <span data-ttu-id="1cc50-174">Para usar uma agenda pré-definida de horário comercial, clique em **Usar uma agenda predefinida** e selecione a agenda que deseja usar na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="1cc50-174">To use a predefined schedule of business hours, click **Use a preset schedule**, and then select the schedule you want to use from the drop-down list.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1cc50-175">Você deve ter definido no mínimo uma agenda predefinida anteriormente para selecionar esta opção.</span><span class="sxs-lookup"><span data-stu-id="1cc50-175">You must have defined at least one preset schedule previously to be able to select this option.</span></span> <span data-ttu-id="1cc50-176">É possível definir agendamentos de predefinições usando o cmdlet <STRONG>New-CSRgsHoursOfBusiness</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-176">You define preset schedules by using the <STRONG>New-CSRgsHoursOfBusiness</STRONG> cmdlet.</span></span> <span data-ttu-id="1cc50-177">Para obter detalhes, consulte <A href="lync-server-2013-optional-define-response-group-business-hours.md">(opcional) definir o horário comercial do grupo de resposta no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-177">For details, see <A href="lync-server-2013-optional-define-response-group-business-hours.md">(Optional) Define Response Group business hours in Lync Server 2013</A>.</span></span>

        
        </div>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1cc50-178">Ao selecionar uma agenda predefinida, <STRONG>Dia</STRONG>, <STRONG>Abertura</STRONG> e <STRONG>Fechamento</STRONG> são automaticamente preenchidos com os dias e horas em que o grupo de resposta está disponível.</span><span class="sxs-lookup"><span data-stu-id="1cc50-178">When you select a preset schedule, <STRONG>Day</STRONG>, <STRONG>Open</STRONG>, and <STRONG>Close</STRONG> are automatically filled with the days and hours that the response group is available.</span></span>

        
        </div>
    
      - <span data-ttu-id="1cc50-179">Para usar uma agenda personalizada que se aplique somente a este fluxo de trabalho, clique em **Usar uma agenda personalizada**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-179">To use a custom schedule that applies only to this workflow, click **Use a custom schedule**.</span></span>

20. <span data-ttu-id="1cc50-180">Se estiver criando uma agenda personalizada para este fluxo de trabalho, clique nas opções para os dias da semana em que o grupo de resposta estará disponível.</span><span class="sxs-lookup"><span data-stu-id="1cc50-180">If you are creating a custom schedule for this workflow, click the check boxes for the days of the week that the response group is available.</span></span>

21. <span data-ttu-id="1cc50-181">Se estiver criando uma agenda personalizada, digite as horas de **Abertura** e **Fechamento** para cada dia da semana em que o grupo de resposta estará disponível.</span><span class="sxs-lookup"><span data-stu-id="1cc50-181">If you are creating a custom schedule, type the **Open** and **Close** hours for each day of the week that the response group available.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-p119">As horas de <STRONG>Abertura</STRONG> e <STRONG>Fechamento</STRONG> devem estar na notação de 24 horas. Por exemplo, se seu escritório funciona em dias úteis das 9 às 5 e fecha ao meio dia para o almoço, o horário comercial é especificado como <STRONG>Abertura</STRONG> 9:00, <STRONG>Fechamento</STRONG> 12:00, <STRONG>Abertura</STRONG> 13:00 e <STRONG>Fechamento</STRONG> 17:00.</span><span class="sxs-lookup"><span data-stu-id="1cc50-p119">The <STRONG>Open</STRONG> and <STRONG>Close</STRONG> hours must be in 24-hour time notation. For example, if your office works a 9-to-5 work day and closes at noon for lunch, the business hours are specified as <STRONG>Open</STRONG> 9:00, <STRONG>Close</STRONG> 12:00, <STRONG>Open</STRONG> 13:00, and <STRONG>Close</STRONG> 17:00.</span></span>

    
    </div>

22. <span data-ttu-id="1cc50-184">Se você desejar reproduzir uma mensagem quando o escritório não estiver aberto, selecione a opção **Reproduzir uma mensagem quando o grupo de resposta estiver fora do horário comercial** e especifique a mensagem a ser reproduzida executando um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="1cc50-184">If you want to play a message when the office is not open, select the **Play a message when the response group is outside of business hours** check box, and then specify the message to play by doing one of the following:</span></span>
    
      - <span data-ttu-id="1cc50-185">Para inserir as mensagem como um texto a ser convertido para fala para o chamador, clique em **Usar conversão de texto para fala** e digite a mensagem na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="1cc50-185">To enter the message as text that is converted to speech for the caller, click **Use text-to-speech**, and then type the message in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1cc50-p120">Não inclua tags HTML no texto digitado. Se você incluir tags HTML, receberá uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="1cc50-p120">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
    
      - <span data-ttu-id="1cc50-p121">Para usar uma gravação de arquivo de áudio para a mensagem, clique em **Selecionar uma gravação**. Se você deseja carregar um novo arquivo de áudio, clique no link **uma gravação**. Na nova janela do navegador, clique em **Procurar**, selecione o arquivo que deseja usar e clique em **Abrir**. Clique em **Carregar** para carregar o arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="1cc50-p121">To use an audio file recording for the message, click **Select a recording**. If you want to upload a new audio file, click the **a recording** link. In the new browser window, click **Browse**, select the file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1cc50-192">Todos os arquivos de áudio fornecidos pelo usuário devem estar de acordo com determinados requisitos.</span><span class="sxs-lookup"><span data-stu-id="1cc50-192">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="1cc50-193">Para obter detalhes sobre os formatos de arquivo de áudio com suporte, consulte <A href="lync-server-2013-technical-requirements-for-response-group.md">requisitos técnicos para o grupo de resposta no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-193">For details about supported audio file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

23. <span data-ttu-id="1cc50-194">Especifique como tratar chamadas após a reprodução da mensagem (se uma mensagem estiver configurada):</span><span class="sxs-lookup"><span data-stu-id="1cc50-194">Specify how to handle calls after the message is played (if a message is configured):</span></span>
    
      - <span data-ttu-id="1cc50-195">Para desconectar a chamada, clique em **Desconectar Chamada**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-195">To disconnect the call, click **Disconnect Call**.</span></span>
    
      - <span data-ttu-id="1cc50-196">Para encaminhar a chamada para a caixa postal, clique em **Encaminhar para caixa postal** e digite o endereço da caixa postal.</span><span class="sxs-lookup"><span data-stu-id="1cc50-196">To forward the call to voice mail, click **Forward to voice mail**, and then type the voice mail address.</span></span> <span data-ttu-id="1cc50-197">O formato do endereço de correio de voz é \<username\> @ \<domainName\> (por exemplo, Bob@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="1cc50-197">The format for the voice mail address is \<username\>@\<domainName\> (for example, bob@contoso.com).</span></span>
    
      - <span data-ttu-id="1cc50-198">Para encaminhar a chamada para outro usuário, clique em **Encaminhar para URI do SIP** e digite um endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="1cc50-198">To forward the call to another user, click **Forward to SIP URI**, and then type a user address.</span></span> <span data-ttu-id="1cc50-199">O formato do endereço de usuário é \<username\> @ \<domainName\> .</span><span class="sxs-lookup"><span data-stu-id="1cc50-199">The format for the user address is \<username\>@\<domainName\>.</span></span>
    
      - <span data-ttu-id="1cc50-200">Para encaminhar a chamada para outro número de telefone, clique em **Encaminhar para número de telefone** e digite o número de telefone.</span><span class="sxs-lookup"><span data-stu-id="1cc50-200">To forward the call to another telephone number, click **Forward to telephone number**, and then type the telephone number.</span></span> <span data-ttu-id="1cc50-201">O formato do número de telefone é \<number\> @ \<domainName\> (por exemplo, + 14255550121@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="1cc50-201">The format for the telephone number is \<number\>@\<domainName\> (for example, +14255550121@contoso.com).</span></span> <span data-ttu-id="1cc50-202">O nome do domínio é usado para encaminhar o chamador ao destino correto.</span><span class="sxs-lookup"><span data-stu-id="1cc50-202">The domain name is used to route the caller to the correct destination.</span></span>

24. <span data-ttu-id="1cc50-203">Sob **Etapa 5 Especifique seus Feriados**, clique nas opções para um ou mais conjuntos de feriados que definem quando o grupo de resposta estará fechado para negócios.</span><span class="sxs-lookup"><span data-stu-id="1cc50-203">Under **Step 5 Specify Your Holidays**, click the check boxes for one or more sets of holidays that define the days when the response group is closed for business.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-204">É necessário definir feriados e conjuntos de feriados antes de configurar o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1cc50-204">You need to define holidays and holiday sets before you configure the workflow.</span></span> <span data-ttu-id="1cc50-205">Use os cmdlets <STRONG>New-CsRgsHoliday</STRONG> e <STRONG>New-CsRgsHolidaySet</STRONG> para definir feriados e conjuntos de feriados.</span><span class="sxs-lookup"><span data-stu-id="1cc50-205">Use the <STRONG>New-CsRgsHoliday</STRONG> and <STRONG>New-CsRgsHolidaySet</STRONG> cmdlets to define holidays and holiday sets.</span></span> <span data-ttu-id="1cc50-206">Para obter detalhes, consulte <A href="lync-server-2013-optional-define-response-group-holiday-sets.md">(opcional) definir os conjuntos de feriados do grupo de resposta no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-206">For details, see <A href="lync-server-2013-optional-define-response-group-holiday-sets.md">(Optional) Define Response Group holiday sets in Lync Server 2013</A>.</span></span>

    
    </div>

25. <span data-ttu-id="1cc50-207">Se você deseja reproduzir uma mensagem nos feriados, selecione a opção **Reproduzir uma mensagem durante os feriados** e especifique a mensagem a ser executada realizado um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="1cc50-207">If you want to play a message on holidays, select the **Play a message during holidays** check box, and then specify the message to play by doing one of the following:</span></span>
    
      - <span data-ttu-id="1cc50-208">Para inserir as mensagem como um texto a ser convertido para fala para o chamador, clique em **Usar conversão de texto para fala** e digite a mensagem na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="1cc50-208">To enter the message as text that is converted to speech for the caller, click **Use text-to-speech**, and then type the message in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1cc50-p127">Não inclua tags HTML no texto digitado. Se você incluir tags HTML, receberá uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="1cc50-p127">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
    
      - <span data-ttu-id="1cc50-p128">Para usar uma gravação de arquivo de áudio para a mensagem, clique em **Selecionar uma gravação**. Se você deseja carregar um novo arquivo de áudio, clique no link **uma gravação**. Na nova janela do navegador, clique em **Procurar**, selecione o arquivo que deseja usar e clique em **Abrir**. Clique em **Carregar** para carregar o arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="1cc50-p128">To use an audio file recording for the message, click **Select a recording**. If you want to upload a new audio file, click the **a recording** link. In the new browser window, click **Browse**, select the file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1cc50-215">Todos os arquivos de áudio fornecidos pelo usuário devem estar de acordo com determinados requisitos.</span><span class="sxs-lookup"><span data-stu-id="1cc50-215">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="1cc50-216">Para obter detalhes sobre os formatos de arquivo de áudio com suporte, consulte <A href="lync-server-2013-technical-requirements-for-response-group.md">requisitos técnicos para o grupo de resposta no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-216">For details about supported audio file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

26. <span data-ttu-id="1cc50-217">Especifique como tratar chamadas após a reprodução da mensagem (se uma mensagem estiver configurada):</span><span class="sxs-lookup"><span data-stu-id="1cc50-217">Specify how to handle calls after the message is played (if a message is configured):</span></span>
    
      - <span data-ttu-id="1cc50-218">Para desconectar a chamada, clique em **Desconectar Chamada**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-218">To disconnect the call, click **Disconnect Call**.</span></span>
    
      - <span data-ttu-id="1cc50-219">Para encaminhar a chamada para a caixa postal, clique em **Encaminhar para caixa postal** e digite o endereço da caixa postal.</span><span class="sxs-lookup"><span data-stu-id="1cc50-219">To forward the call to voice mail, click **Forward to voice mail**, and then type the voice mail address.</span></span> <span data-ttu-id="1cc50-220">O formato do endereço de correio de voz é \<username\> @ \<domainName\> (por exemplo, Bob@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="1cc50-220">The format for the voice mail address is \<username\>@\<domainName\> (for example, bob@contoso.com).</span></span>
    
      - <span data-ttu-id="1cc50-221">Para encaminhar a chamada para outro usuário, clique em **Encaminhar para URI do SIP** e digite um endereço de usuário.</span><span class="sxs-lookup"><span data-stu-id="1cc50-221">To forward the call to another user, click **Forward to SIP URI**, and then type a user address.</span></span> <span data-ttu-id="1cc50-222">O formato do endereço de usuário é \<username\> @ \<domainName\> .</span><span class="sxs-lookup"><span data-stu-id="1cc50-222">The format for the user address is \<username\>@\<domainName\>.</span></span>
    
      - <span data-ttu-id="1cc50-223">Para encaminhar a chamada para outro número de telefone, clique em **Encaminhar para número de telefone** e digite o número de telefone.</span><span class="sxs-lookup"><span data-stu-id="1cc50-223">To forward the call to another telephone number, click **Forward to telephone number**, and then type the telephone number.</span></span> <span data-ttu-id="1cc50-224">O formato do número de telefone é \<number\> @ \<domainName\> (por exemplo, + 14255550121@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="1cc50-224">The format for the telephone number is \<number\>@\<domainName\> (for example, +14255550121@contoso.com).</span></span> <span data-ttu-id="1cc50-225">O nome do domínio é usado para encaminhar o chamador ao destino correto.</span><span class="sxs-lookup"><span data-stu-id="1cc50-225">The domain name is used to route the caller to the correct destination.</span></span>

27. <span data-ttu-id="1cc50-226">Sob **Etapa 6 Configure uma Fila**, em **Selecione a fila que receberá as chamadas**, selecione a fila que você deseja que segure as chamadas até que um operador torne-se disponível.</span><span class="sxs-lookup"><span data-stu-id="1cc50-226">Under **Step 6 Configure a Queue**, in **Select the queue that will receive the calls**, select the queue that you want to hold callers until an agent becomes available.</span></span>

28. <span data-ttu-id="1cc50-227">Sob **Etapa 7 Configure Música de Espera**, escolha a música que deseja que os chamadores ouçam enquanto esperam que um operador, executando um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="1cc50-227">Under **Step 7 Configure Music on Hold**, choose the music you want callers to listen to while waiting for an agent by doing one of the following:</span></span>
    
      - <span data-ttu-id="1cc50-228">Para usar a gravação padrão de música de espera, clique em **Usar padrão**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-228">To use the default music-on-hold recording, click **Use default**.</span></span>
    
      - <span data-ttu-id="1cc50-p133">Para usar uma gravação de arquivo de áudio para a música de espera, clique em **Selecionar um arquivo de música**. Se você deseja carregar um novo arquivo de áudio, clique no link **um arquivo de música**. Na nova janela do navegador, clique em **Procurar**, selecione o arquivo que deseja usar e clique em **Abrir**. Clique em **Carregar** para carregar o arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="1cc50-p133">To use an audio file recording for the music on hold, click **Select a music file**. If you want to upload a new audio file, click the **a music file** link. In the new browser window, click **Browse**, select the file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="1cc50-233">Todos os arquivos de áudio fornecidos pelo usuário devem atender determinados requisitos.</span><span class="sxs-lookup"><span data-stu-id="1cc50-233">All user provided audio files must meet certain requirements.</span></span> <span data-ttu-id="1cc50-234">Para obter detalhes sobre os formatos de arquivo de áudio com suporte, consulte <A href="lync-server-2013-technical-requirements-for-response-group.md">requisitos técnicos para o grupo de resposta no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-234">For details about supported audio file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

29. <span data-ttu-id="1cc50-235">Clique em **Implantar**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-235">Click **Deploy**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-create-or-modify-a-hunt-group-workflow"></a><span data-ttu-id="1cc50-236">Para usar o Windows PowerShell para criar ou modificar um fluxo de trabalho de grupo coletivo</span><span class="sxs-lookup"><span data-stu-id="1cc50-236">To use Windows PowerShell to create or modify a hunt group workflow</span></span>

1.  <span data-ttu-id="1cc50-237">Faça logon como um membro do grupo RTCUniversalServerAdmins ou como um membro de uma das funções administrativas predefinidas que oferecem suporte ao Grupo de Resposta.</span><span class="sxs-lookup"><span data-stu-id="1cc50-237">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="1cc50-238">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-238">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="1cc50-p135">Crie o prompt a ser reproduzido na mensagem de boas-vindas e salve-o como uma variável. Na linha de comando, execute:</span><span class="sxs-lookup"><span data-stu-id="1cc50-p135">Create the prompt to be played for the welcome message, and save it in a variable. At the command line, run:</span></span>
    
        $promptWM = New-CsRgsPrompt -TextToSpeechPrompt "<text for TTS prompt>"
    
    <span data-ttu-id="1cc50-241">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1cc50-241">For example:</span></span>
    
        $promptWM = New-CsRgsPrompt -TextToSpeechPrompt "Welcome to Contoso. Please wait for an available agent."
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-242">Para usar um arquivo de áudio no prompt, use o cmdlet <STRONG>Import-CsRgsAudioFile</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-242">To use an audio file for the prompt, use the <STRONG>Import-CsRgsAudioFile</STRONG> cmdlet.</span></span> <span data-ttu-id="1cc50-243">Para obter detalhes, consulte <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">importar-CsRgsAudioFile</A>.</span><span class="sxs-lookup"><span data-stu-id="1cc50-243">For details, see <A href="https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile">Import-CsRgsAudioFile</A>.</span></span>

    
    </div>

4.  <span data-ttu-id="1cc50-244">Obtenha a identidade da fila ou pergunta onde as chamadas serão direcionadas.</span><span class="sxs-lookup"><span data-stu-id="1cc50-244">Get the identity of the queue or question where the calls will be directed.</span></span> <span data-ttu-id="1cc50-245">Na linha de comando, execute:</span><span class="sxs-lookup"><span data-stu-id="1cc50-245">At the command line, run:</span></span>
    
        $qid = (Get-CsRgsQueue -Name "Help Desk").Identity
    
    <span data-ttu-id="1cc50-246">Para obter detalhes sobre como criar a fila, consulte [New-CsRgsQueue](https://docs.microsoft.com/powershell/module/skype/New-CsRgsQueue).</span><span class="sxs-lookup"><span data-stu-id="1cc50-246">For details about creating the queue, see [New-CsRgsQueue](https://docs.microsoft.com/powershell/module/skype/New-CsRgsQueue).</span></span>

5.  <span data-ttu-id="1cc50-p138">Defina a ação padrão a ser realizada quando um fluxo de trabalho é aberto durante o horário comercial e salve-o em uma variável. Na linha de comando, execute:</span><span class="sxs-lookup"><span data-stu-id="1cc50-p138">Define the default action to be taken when a workflow is opened during business hours, and save it in a variable. At the command line, run:</span></span>
    
        $actionWM = New-CsRgsCallAction -Prompt <saved prompt from previous step> -Action <action to be taken> -QueueID $qid
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-p139">Para fluxos de trabalho do grupo de busca, a ação padrão deve direcionar a chamada para uma fila. Este parâmetro é necessário para fluxos de trabalho ativos. Não é necessário para fluxos de trabalho inativos.</span><span class="sxs-lookup"><span data-stu-id="1cc50-p139">For hunt group workflows, the default action must direct the call to a queue. This is parameter is required for active workflows. It is not required for inactive workflows.</span></span>

    
    </div>
    
    <span data-ttu-id="1cc50-252">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1cc50-252">For example:</span></span>
    
        $actionWM = New-CsRgsCallAction -Prompt $promptWM -Action TransferToQueue -QueueID $qid.Identity

6.  <span data-ttu-id="1cc50-253">Se você deseja definir o horário comercial e feriados, é necessário criá-los antes de criar ou modificar o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1cc50-253">If you want to define business hours and holidays, you need to create them before you create or modify the workflow.</span></span> <span data-ttu-id="1cc50-254">Para obter detalhes, consulte [(opcional) definir o grupo de resposta horário comercial no Lync server 2013](lync-server-2013-optional-define-response-group-business-hours.md) e [(opcional) definir os conjuntos de feriados do grupo de resposta no Lync Server 2013](lync-server-2013-optional-define-response-group-holiday-sets.md).</span><span class="sxs-lookup"><span data-stu-id="1cc50-254">For details, see [(Optional) Define Response Group business hours in Lync Server 2013](lync-server-2013-optional-define-response-group-business-hours.md) and [(Optional) Define Response Group holiday sets in Lync Server 2013](lync-server-2013-optional-define-response-group-holiday-sets.md).</span></span>

7.  <span data-ttu-id="1cc50-255">Se você deseja ter prompts para chamadas recebidas fora do horário comercial ou em feriados, use o cmdlet **New-CsRgsPrompt** para definir o prompt e use o **New-CsRgsCallAction** para definir a ação a ser realizada após o prompt.</span><span class="sxs-lookup"><span data-stu-id="1cc50-255">If you want to have prompts for calls that are received out of business hours or on holidays, use the **New-CsRgsPrompt** cmdlet to define the prompt, and use the **New-CsRgsCallAction** to define the action to be taken after the prompt.</span></span> <span data-ttu-id="1cc50-256">Para obter detalhes, consulte [New-CsRgsPrompt](https://docs.microsoft.com/powershell/module/skype/New-CsRgsPrompt) and [New-CsRgsCallAction](https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction).</span><span class="sxs-lookup"><span data-stu-id="1cc50-256">For details, see [New-CsRgsPrompt](https://docs.microsoft.com/powershell/module/skype/New-CsRgsPrompt) and [New-CsRgsCallAction](https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction).</span></span>

8.  <span data-ttu-id="1cc50-257">Recupere o nome do serviço do serviço de grupo de resposta do Lync Server e atribua-o a uma variável.</span><span class="sxs-lookup"><span data-stu-id="1cc50-257">Retrieve the service name for the Lync Server Response Group service and assign it to a variable.</span></span> <span data-ttu-id="1cc50-258">No comando, execute:</span><span class="sxs-lookup"><span data-stu-id="1cc50-258">At the command, run:</span></span>
    
        $serviceId="service:"+(Get-CSService | ?{$_.Applications -like "*RGS*"}).ServiceId;

9.  <span data-ttu-id="1cc50-259">Crie ou modifique o fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1cc50-259">Create or modify the workflow.</span></span> <span data-ttu-id="1cc50-260">Para criar um fluxo de trabalho, use **New-CsRgsWorkflow**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-260">To create a workflow, use **New-CsRgsWorkflow**.</span></span> <span data-ttu-id="1cc50-261">Para modificar um fluxo de trabalho, use **set-CsRgsWorkflow**.</span><span class="sxs-lookup"><span data-stu-id="1cc50-261">To modify a workflow, use **Set-CsRgsWorkflow**.</span></span> <span data-ttu-id="1cc50-262">Na linha de comando, digite:</span><span class="sxs-lookup"><span data-stu-id="1cc50-262">At the command line, type:</span></span>
    
        $workflowHG = New-CsRgsWorkflow -Parent <service ID for the Response Group service> -Name "<hunt group name>" [-Description "<hunt group description>"] -PrimaryUri "<SIP address for the workflow>" [-LineUri "<Phone number for the workflow>"] [-DisplayNumber "<Phone number displayed in Lync>"] [-Active <$true | $false>] [-Anonymous <$true | $false>] [-DefaultAction <variable from preceding step>] [-EnabledForFederation <$true | $false>] [-Managed <$true | $false>] [-MangersByUri <SIP addresses for Response Group Managers who can manage the workflow>]
    
    <span data-ttu-id="1cc50-263">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1cc50-263">For example:</span></span>
    
        $workflowHG = New-CsRgsWorkflow -Parent $serviceID -Name "Human Resources" -Description "Human Resources workflow" -PrimaryUri "sip:humanresources@contoso.com" -LineUri "TEL:+14255551219" -DisplayNumber "555-1219" -Active $true -Anonymous $true -DefaultAction $actionWM -EnabledForFederation $false -Managed $true -ManagersByUri "sip:bob@contoso.com", "mindy@contoso.com"
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="1cc50-264">Todos os usuários que são gerentes para fluxos de trabalho devem ser atribuídos à função CsResponseGroupManager.</span><span class="sxs-lookup"><span data-stu-id="1cc50-264">All users who are designated managers for workflows must be assigned the CsResponseGroupManager role.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1cc50-265">Para obter detalhes sobre parâmetros opcionais adicionais, consulte <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsWorkflow">New-CsRgsWorkflow</A> ou <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsRgsWorkflow">set-CsRgsWorkflow</A></span><span class="sxs-lookup"><span data-stu-id="1cc50-265">For details about additional optional parameters, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsRgsWorkflow">New-CsRgsWorkflow</A> or <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsRgsWorkflow">Set-CsRgsWorkflow</A></span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1cc50-266">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cc50-266">See Also</span></span>


[<span data-ttu-id="1cc50-267">Adicionais Definir conjuntos de feriados do grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cc50-267">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)  


[<span data-ttu-id="1cc50-268">Adicionais Definir o horário comercial do grupo de resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1cc50-268">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)  


[<span data-ttu-id="1cc50-269">New-CsRgsWorkflow</span><span class="sxs-lookup"><span data-stu-id="1cc50-269">New-CsRgsWorkflow</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsWorkflow)  
[<span data-ttu-id="1cc50-270">Set-CsRgsWorkflow</span><span class="sxs-lookup"><span data-stu-id="1cc50-270">Set-CsRgsWorkflow</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsRgsWorkflow)  
[<span data-ttu-id="1cc50-271">New-CsRgsPrompt</span><span class="sxs-lookup"><span data-stu-id="1cc50-271">New-CsRgsPrompt</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsPrompt)  
[<span data-ttu-id="1cc50-272">New-CsRgsCallAction</span><span class="sxs-lookup"><span data-stu-id="1cc50-272">New-CsRgsCallAction</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsRgsCallAction)  
  

<span data-ttu-id="1cc50-273"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1cc50-273"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

