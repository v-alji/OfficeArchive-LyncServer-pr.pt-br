---
title: 'Lync Server 2013: criar ou modificar um intervalo de números não atribuídos'
description: 'Lync Server 2013: criar ou modificar um intervalo numérico não atribuído.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify an unassigned number range
ms:assetid: a102b226-0460-4d5c-82f9-79b8444fa958
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412748(v=OCS.15)
ms:contentKeyID: 48185013
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2998616b931e94c9c38fc44d569b84b3af37709d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431656"
---
# <a name="create-or-modify-an-unassigned-number-range-in-lync-server-2013"></a><span data-ttu-id="39941-103">Criar ou modificar um intervalo de números não atribuídos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39941-103">Create or modify an unassigned number range in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39941-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39941-104">

<span> </span></span></span>

<span data-ttu-id="39941-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="39941-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="39941-106">Use um dos procedimentos a seguir para configurar intervalos de números não atribuídos para o aplicativo de anúncio.</span><span class="sxs-lookup"><span data-stu-id="39941-106">Use one of the following procedures to configure unassigned number ranges for the Announcement application.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="39941-107">Antes de configurar a tabela de números não atribuídas, você já deve ter definido um ou mais comunicados ou configurar um atendedor automático de UM (Unificação de mensagens) do Exchange.</span><span class="sxs-lookup"><span data-stu-id="39941-107">Before you configure the unassigned number table, you must have already defined one or more announcements or set up an Exchange Unified Messaging (UM) Auto Attendant.</span></span>



</div>

<div>

## <a name="to-use-lync-server-control-panel-to-configure-unassigned-phone-numbers"></a><span data-ttu-id="39941-108">Para usar o painel de controle do Lync Server para configurar números de telefone não atribuídos</span><span class="sxs-lookup"><span data-stu-id="39941-108">To use Lync Server Control Panel to configure unassigned phone numbers</span></span>

1.  <span data-ttu-id="39941-109">Faça logon no computador como um membro do grupo RTCUniversalServerAdmins ou como um membro da função CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="39941-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="39941-110">Para obter detalhes, consulte [delegar permissões de configuração no Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="39941-110">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="39941-111">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="39941-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="39941-112">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="39941-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="39941-113">Na barra de navegação à esquerda, clique em **Recursos de Voz** e depois, em **Número Não Atribuído**.</span><span class="sxs-lookup"><span data-stu-id="39941-113">In the left navigation bar, click **Voice Features**, and then click **Unassigned Number**.</span></span>

4.  <span data-ttu-id="39941-114">Na página **Números não atribuídos**, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="39941-114">On the **Unassigned Number** page, do one of the following:</span></span>
    
      - <span data-ttu-id="39941-p103">Para criar um novo intervalo de números, clique em **Novo**. Em **Nome**, digite o nome que identifica este intervalo de números.</span><span class="sxs-lookup"><span data-stu-id="39941-p103">To create a new number range, click **New**. In **Name**, type an identifying name for this range of numbers.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="39941-117">Depois de confirmar o novo intervalo de números não atribuídos para o banco de dados, não é possível alterar este nome.</span><span class="sxs-lookup"><span data-stu-id="39941-117">After you commit the new unassigned number range to the database, you cannot change this name.</span></span>

        
        </div>
    
      - <span data-ttu-id="39941-p104">Para modificar um intervalo de números existente, digite todo o nome do intervalo de órbita, ou parte dele, no campo de pesquisa. Na lista de resultados de intervalos de número, clique no nome desejado, clique em **Editar** e depois, clique em **Exibir Detalhes**.</span><span class="sxs-lookup"><span data-stu-id="39941-p104">To modify an existing number range, type all or part of the name of the number range in the search field. In the resulting list of number ranges, click the name you want, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="39941-120">No primeiro campo **Intervalo Numérico**, digite o número inicial do intervalo e no segundo campo **Intervalo Numérico** digite o número final do intervalo.</span><span class="sxs-lookup"><span data-stu-id="39941-120">In the first **Number range** field, type the beginning number of the range, and in the second **Number range** field, type the ending number of the range.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="39941-121">O número inicial do intervalo deve ser menor ou igual ao número final.</span><span class="sxs-lookup"><span data-stu-id="39941-121">The beginning number of the range must be less than or equal to the ending number of the range.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="39941-122">Se o número inicial ou o número final do intervalo incluir um número de ramal, ambos os números devem incluir um ramal, que deve ser o mesmo para ambos.</span><span class="sxs-lookup"><span data-stu-id="39941-122">If the beginning number of the range or the ending number of the range includes an extension number, both the beginning number and the ending number of the range must include an extension, and the extension number must be the same for both the beginning number and the ending number.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="39941-123">O número deve corresponder à expressão regular (Tel:)? ( \+ )? [1-9] \d {0,17} (; Ext = [1-9] \d {0,9} )?.</span><span class="sxs-lookup"><span data-stu-id="39941-123">The number must match the regular expression (tel:)?(\+)?[1-9]\d{0,17}(;ext=[1-9]\d{0,9})?.</span></span> <span data-ttu-id="39941-124">Isso significa que o número pode começar com a cadeia de caracteres tel: (se você não especificar essa cadeia de caracteres, ela será adicionada automaticamente), um sinal de adição (+) e um dígito de 1 a 9.</span><span class="sxs-lookup"><span data-stu-id="39941-124">This means the number may begin with the string tel: (if you don’t specify that string, it will be automatically added for you), a plus sign (+), and a digit 1 through 9.</span></span> <span data-ttu-id="39941-125">O número de telefone pode ter até 17 dígitos e pode ser seguido de um ramal no formato ;ext= seguido do número do ramal.</span><span class="sxs-lookup"><span data-stu-id="39941-125">The phone number can be up to 17 digits and may be followed by an extension in the format ;ext= followed by the extension number.</span></span></P></LI></UL>

    
    </div>

6.  <span data-ttu-id="39941-126">Em **Serviço de Comunicado**, execute um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="39941-126">In **Announcement service**, do one of the following:</span></span>
    
      - <span data-ttu-id="39941-127">Clique em **Comunicado**.</span><span class="sxs-lookup"><span data-stu-id="39941-127">Click **Announcement**.</span></span>
    
      - <span data-ttu-id="39941-128">Clique em **UM do Exchange**.</span><span class="sxs-lookup"><span data-stu-id="39941-128">Click **Exchange UM**.</span></span>

7.  <span data-ttu-id="39941-129">Se, na etapa anterior, você clicou em **Comunicado**, execute:</span><span class="sxs-lookup"><span data-stu-id="39941-129">If, in the previous step, you clicked **Announcement**, do the following:</span></span>
    
    1.  <span data-ttu-id="39941-130">Em **FQDN do servidor de destino**, clique em **selecionar**, clique na ID de serviço do serviço de aplicativo que executa o aplicativo de anúncio que manipulará as chamadas de entrada para esse intervalo de números não atribuídos e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="39941-130">Under **FQDN of destination server**, click **Select**, click the service ID of the Application service that runs the Announcement application that will handle incoming calls to this range of unassigned numbers, and then click **OK**.</span></span>
    
    2.  <span data-ttu-id="39941-131">Em **Comunicado**, clique no comunicado a ser reproduzido para este intervalo de números não atribuídos.</span><span class="sxs-lookup"><span data-stu-id="39941-131">In **Announcement**, click the announcement to be played for this range of unassigned numbers.</span></span>

8.  <span data-ttu-id="39941-132">Se, na etapa anterior, você clicou em **UM do Exchange**, sob **Número de telefone do Atendedor Automático**, clique em **Selecionar**, clique no número de telefone a ser usado para este intervalo de números não atribuídos e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="39941-132">If, in the previous step, you clicked **Exchange UM**, under **Auto Attendant phone number**, click **Select**, click the phone number to be used for this range of unassigned numbers, and then click **OK**.</span></span>

9.  <span data-ttu-id="39941-133">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="39941-133">Click **OK**.</span></span>

10. <span data-ttu-id="39941-p106">Na página **Número Não Atribuído**, certifique-se de que os intervalos numéricos não atribuídos estejam organizados da ordem que você deseja. Para alterar a posição do intervalo na tabela, clique em um ou mais nomes consecutivos na lista de intervalos e clique na seta para cima ou para baixo.</span><span class="sxs-lookup"><span data-stu-id="39941-p106">On the **Unassigned Number** page, be sure that the unassigned number ranges are arranged in the order that you want. To change a range's position in the table, click one or more consecutive names in the list of ranges, and then click the up arrow or the down arrow.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="39941-136">O Lync Server procura a tabela número não atribuído da parte superior para a inferior e usa o primeiro intervalo que corresponde ao número não atribuído.</span><span class="sxs-lookup"><span data-stu-id="39941-136">Lync Server searches the unassigned number table from top to bottom and uses the first range that matches the unassigned number.</span></span> <span data-ttu-id="39941-137">Se você tem intervalos sobrepostos e um intervalo que especifica uma última ação de reclassificação, certifique-se de que o intervalo esteja no final da lista.</span><span class="sxs-lookup"><span data-stu-id="39941-137">If you have overlapping ranges and one range specifies a last resort action, make sure that range is at the bottom of the list.</span></span>

    
    </div>

11. <span data-ttu-id="39941-138">Quando os intervalos numéricos não atribuídos estiverem na ordem desejada, clique em **Confirmar tudo**.</span><span class="sxs-lookup"><span data-stu-id="39941-138">When you have the unassigned number ranges in the order that you want, click **Commit all**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-configure-unassigned-phone-numbers"></a><span data-ttu-id="39941-139">Para usar o Windows PowerShell para configurar números de telefone não atribuídos</span><span class="sxs-lookup"><span data-stu-id="39941-139">To use Windows PowerShell to configure unassigned phone numbers</span></span>

1.  <span data-ttu-id="39941-140">Faça logon no computador em que o Shell de gerenciamento do Lync Server está instalado como membro do grupo RTCUniversalServerAdmins ou com os direitos de usuário necessários, conforme descrito em [permissões de configuração de representante no Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="39941-140">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="39941-141">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="39941-141">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="39941-142">Use **New-CsUnassignedNumber** para criar um intervalo de números não atribuídos.</span><span class="sxs-lookup"><span data-stu-id="39941-142">Use **New-CsUnassignedNumber** to create a new unassigned number range.</span></span> <span data-ttu-id="39941-143">Use **Set-CsUnassignedNumber** para modificar um intervalo de números não atribuídos existente.</span><span class="sxs-lookup"><span data-stu-id="39941-143">Use **Set-CsUnassignedNumber** to modify an existing unassigned number range.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="39941-p109">Se você tiver intervalos sobrepostos e desejar que os intervalos sejam aplicados em uma ordem específica, inclua o parâmetro Prioridade. O intervalo com a maior prioridade será aplicado à chamada.</span><span class="sxs-lookup"><span data-stu-id="39941-p109">If you have overlapping ranges and want the ranges to be applied in a specific order, include the Priority parameter. The range with the highest priority will be applied to the call.</span></span>

    
    </div>
    
    <span data-ttu-id="39941-146">No linha de comando, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="39941-146">At the command line, do one of the following:</span></span>
    
      - <span data-ttu-id="39941-147">Para criar um intervalo numérico para um serviço de Comunicado, execute:</span><span class="sxs-lookup"><span data-stu-id="39941-147">To create a number range for an Announcement service, run:</span></span>
        
            New-CsUnassignedNumber -Identity <unique identifier for unassigned number range> -NumberRangeStart <first number in range> -NumberRangeEnd <last number in range> -AnnouncementName <announcement name> -AnnouncementService <FQDN or service ID of the Announcement service>
    
      - <span data-ttu-id="39941-148">Ou para criar um intervalo numérico para Atendedor Automático do UM do Exchange, execute:</span><span class="sxs-lookup"><span data-stu-id="39941-148">Or, to create a number range for Exchange UM Auto Attendant, run:</span></span>
        
            New-CsUnassignedNumber -ExUmAutoAttendantPhoneNumber <phone number> -Identity <unique identifier for unassigned number range> -NumberRangeStart <first number in range> -NumberRangeEnd <last number in range>
    
    <span data-ttu-id="39941-149">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="39941-149">For example:</span></span>
    
        New-CsUnassignedNumber -Identity "Unassigned range 1" -NumberRangeStart "+14255551000" -NumberRangeEnd "+14255551100" -AnnouncementName "Welcome Announcement" -AnnouncementService ApplicationServer:Redmond.contoso.com
    
    <span data-ttu-id="39941-150">Ou</span><span class="sxs-lookup"><span data-stu-id="39941-150">Or</span></span>
    
        New-CsUnassignedNumber -ExUmAutoAttendantPhoneNumber "+12065551234" -Identity "Unassigned range 1" -NumberRangeStart "+14255551000" -NumberRangeEnd "+14255551100"
    
    <span data-ttu-id="39941-151">O exemplo a seguir mostra como modificar os números em um intervalo numérico não atribuído existente.</span><span class="sxs-lookup"><span data-stu-id="39941-151">The following example shows how to modify the numbers in an existing unassigned number range:</span></span>
    
        Set-CsUnassignedNumber -Identity "Unassigned range 1" -NumberRangeStart "+14255551000" -NumberRangeEnd "+14255551900"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="39941-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="39941-152">See Also</span></span>


[<span data-ttu-id="39941-153">Excluir um intervalo de números não atribuído no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39941-153">Delete an unassigned number range in Lync Server 2013</span></span>](lync-server-2013-delete-an-unassigned-number-range.md)  


[<span data-ttu-id="39941-154">New-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="39941-154">New-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsUnassignedNumber)  
[<span data-ttu-id="39941-155">Set-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="39941-155">Set-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsUnassignedNumber)  
[<span data-ttu-id="39941-156">Get-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="39941-156">Get-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUnassignedNumber)  
  

<span data-ttu-id="39941-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39941-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

