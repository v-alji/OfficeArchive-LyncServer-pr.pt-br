---
title: Configurando uma política de qualidade de serviço para seus servidores de borda A/V
description: Configurar uma política de qualidade de serviço para seus servidores de borda A/V.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a Quality of Service policy for your A/V Edge Servers
ms:assetid: 119ee1f5-45b9-40ba-98e5-c694dd2fc5c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204681(v=OCS.15)
ms:contentKeyID: 48183444
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec1f012260aa32df984925a86882a3201e07db0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433504"
---
# <a name="configuring-a-quality-of-service-policy-for-your-av-edge-servers-in-lync-server-2013"></a><span data-ttu-id="50429-103">Configurando uma política de qualidade de serviço para seus servidores de borda A/V no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="50429-103">Configuring a Quality of Service policy for your A/V Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="50429-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="50429-104">

<span> </span></span></span>

<span data-ttu-id="50429-105">_**Tópico da última modificação:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="50429-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="50429-106">Além de criar políticas de QoS para seus servidores de conferência, aplicativo e mediação, você também deve criar políticas de áudio e de vídeo para o lado interno dos seus servidores de borda A/V.</span><span class="sxs-lookup"><span data-stu-id="50429-106">In addition to creating QoS policies for your Conferencing, Application, and Mediation servers, you must also create both audio and video policies for the internal side of your A/V Edge servers.</span></span> <span data-ttu-id="50429-107">No entanto, as políticas usadas em seus servidores de borda são diferentes das políticas usadas em seus servidores de conferência, aplicativo e mediação.</span><span class="sxs-lookup"><span data-stu-id="50429-107">However, the policies used on your Edge servers are different from the policies used on your Conferencing, Application, and Mediation servers.</span></span> <span data-ttu-id="50429-108">Para os servidores de conferência, aplicativo e mediação, você especificou um intervalo de porta de origem; com os servidores de borda, você precisa especificar um intervalo de porta de destino.</span><span class="sxs-lookup"><span data-stu-id="50429-108">For the Conferencing, Application, and Mediation servers you specified a source port range; with Edge servers, you need to specify a destination port range.</span></span> <span data-ttu-id="50429-109">Por isso você não pode simplesmente aplicar as políticas de QoS do servidor de conferência, aplicativo e mediação a seus servidores de borda: essas políticas simplesmente não funcionarão.</span><span class="sxs-lookup"><span data-stu-id="50429-109">Because of that you cannot simply apply the Conferencing, Application, and Mediation server QoS policies to your Edge servers: these policies simply won't work.</span></span> <span data-ttu-id="50429-110">Em vez disso, você deve criar novas políticas e aplicar essas políticas somente a seus servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="50429-110">Instead, you must create new policies and apply those policies to your Edge servers only.</span></span>

<span data-ttu-id="50429-111">O procedimento a seguir descreve o processo de criação de objetos de política de grupo do Active Directory que podem ser usados para gerenciar a qualidade do serviço em servidores Edge.</span><span class="sxs-lookup"><span data-stu-id="50429-111">The following procedure describes the process for creating Active Directory Group Policy objects that can be used to manage Quality of Service on Edge Servers.</span></span> <span data-ttu-id="50429-112">É claro que é possível que seus servidores de borda sejam servidores autônomos que não tenham contas do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50429-112">Of course, it's possible that your Edge servers are stand-alone servers that do not have Active Directory accounts.</span></span> <span data-ttu-id="50429-113">Se esse for o caso, você pode usar a política de grupo local em vez da política de grupo do Active Directory: a única diferença é que você deve criar essas políticas locais usando o editor de política de grupo local e deve criar individualmente o mesmo conjunto de políticas em cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="50429-113">If that's the case, you can use local Group Policy instead of Active Directory Group Policy: the only difference is that you must create these local policies using the Local Group Policy Editor, and must individually create the same set of policies on each Edge Server.</span></span> <span data-ttu-id="50429-114">Para iniciar o editor de política de grupo local em um servidor de borda, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="50429-114">To start the Local Group Policy Editor on an Edge server do the following:</span></span>

1.  <span data-ttu-id="50429-115">Clique em **Iniciar** e em **executar**.</span><span class="sxs-lookup"><span data-stu-id="50429-115">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="50429-116">Na caixa de diálogo **executar** , digite **gpedit. msc** e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="50429-116">In the **Run** dialog box, type **gpedit.msc** and then press ENTER.</span></span>

<span data-ttu-id="50429-117">Se você estiver criando políticas baseadas no Active Directory, faça logon em um computador onde o gerenciamento de política de grupo foi instalado.</span><span class="sxs-lookup"><span data-stu-id="50429-117">If you are creating Active Directory-based policies, then you should log on to a computer where Group Policy Management has been installed.</span></span> <span data-ttu-id="50429-118">Nesse caso, abra gerenciamento de política de grupo (clique em **Iniciar**, aponte para **Ferramentas administrativas** e clique em **Gerenciamento de política de grupo**) e conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="50429-118">In that case, open Group Policy Management (click **Start**, point to **Administrative Tools**, and then click **Group Policy Management**) and then complete the following steps:</span></span>

1.  <span data-ttu-id="50429-119">No gerenciamento de política de grupo, localize o contêiner em que a nova política deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="50429-119">In Group Policy Management, locate the container where the new policy should be created.</span></span> <span data-ttu-id="50429-120">Por exemplo, se todos os seus computadores do Lync Server estiverem localizados em uma OU chamada Lync Server, a nova política deve ser criada na OU do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="50429-120">For example, if all your Lync Server computers are located in an OU named Lync Server then the new policy should be created in the Lync Server OU.</span></span>

2.  <span data-ttu-id="50429-121">Clique com o botão direito do mouse no contêiner apropriado e, em seguida, clique em **criar um GPO neste domínio e vincule-o aqui**.</span><span class="sxs-lookup"><span data-stu-id="50429-121">Right-click the appropriate container and then click **Create a GPO in this domain, and Link it here**.</span></span>

3.  <span data-ttu-id="50429-122">Na caixa de diálogo **novo GPO** , digite um nome para o novo objeto de política de grupo na caixa **nome** (por exemplo, o **áudio do Lync Server**) e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="50429-122">In the **New GPO** dialog box, type a name for the new Group Policy object in the **Name** box (for example, **Lync Server Audio**) and then click **OK**.</span></span>

4.  <span data-ttu-id="50429-123">Clique com o botão direito do mouse na política recém-criada e clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="50429-123">Right-click the newly-created policy and then click **Edit**.</span></span>

<span data-ttu-id="50429-124">Aqui, o processo é idêntico independentemente de você estar criando uma política do Active Directory ou uma política local:</span><span class="sxs-lookup"><span data-stu-id="50429-124">From here the process is identical regardless of whether you are creating an Active Directory policy or a local policy:</span></span>

1.  <span data-ttu-id="50429-125">No editor de gerenciamento de política de grupo ou no editor de política de grupo local, expanda **configuração do computador**, expanda **políticas**, expanda **configurações do Windows**, clique com o botão direito do mouse em **QoS baseada em política** e clique em **criar nova política**.</span><span class="sxs-lookup"><span data-stu-id="50429-125">In the Group Policy Management Editor or the Local Group Policy Editor, expand **Computer Configuration**, expand **Policies**, expand **Windows Settings**, right-click **Policy-based QoS**, and then click **Create new policy**.</span></span>

2.  <span data-ttu-id="50429-126">Na caixa de diálogo **QoS baseada em política** , na página de abertura, digite um nome para a nova política (por exemplo, **áudio do Lync Server**) na caixa **nome** .</span><span class="sxs-lookup"><span data-stu-id="50429-126">In the **Policy-based QoS** dialog box, on the opening page, type a name for the new policy (e.g., **Lync Server Audio**) in the **Name** box.</span></span> <span data-ttu-id="50429-127">Selecione **especificar valor DSCP** e defina o valor como **46**.</span><span class="sxs-lookup"><span data-stu-id="50429-127">Select **Specify DSCP Value** and set the value to **46**.</span></span> <span data-ttu-id="50429-128">Deixe **especificar a taxa de aceleração de saída** desmarcada e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="50429-128">Leave **Specify Outbound Throttle Rate** unselected, and then click **Next**.</span></span>

3.  <span data-ttu-id="50429-129">Na página seguinte, verifique se a opção **todos os aplicativos** está selecionada e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="50429-129">On the next page, make sure that **All applications** is selected and then click **Next**.</span></span> <span data-ttu-id="50429-130">Essa configuração instrui a rede a procurar todos os pacotes com uma marcação DSCP de 46, não apenas pacotes criados por um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="50429-130">This setting instructs the network to look for all packets with a DSCP marking of 46, not just packets created by a specific application.</span></span>

4.  <span data-ttu-id="50429-131">Na terceira página, verifique se **qualquer endereço IP de origem** e **qualquer endereço IP de destino** estão selecionados e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="50429-131">On the third page, make sure that both **Any source IP address** and **Any destination IP address** are selected and then click **Next**.</span></span> <span data-ttu-id="50429-132">Essas duas configurações garantem que os pacotes serão gerenciados independentemente de qual computador (endereço IP) enviou esses pacotes e qual computador (endereço IP) receberá esses pacotes.</span><span class="sxs-lookup"><span data-stu-id="50429-132">These two settings ensure that packets will be managed regardless of which computer (IP address) sent those packets and which computer (IP address) will receive those packets.</span></span>

5.  <span data-ttu-id="50429-133">Na página quatro, selecione **TCP e UDP** na lista **Selecione o protocolo que esta política de QoS se aplica à** lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="50429-133">On page four, select **TCP and UDP** from the **Select the protocol this QoS policy applies to** dropdown list.</span></span> <span data-ttu-id="50429-134">TCP (Transmission Control Protocol) e UDP (User Datagram Protocol) são os dois protocolos de rede mais comumente usados pelo Lync Server e seus aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="50429-134">TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two networking protocols most-commonly used by Lync Server and its client applications.</span></span>

6.  <span data-ttu-id="50429-135">Em título **especifique o número da porta de destino**, selecione uma **destas portas de destino ou intervalo**.</span><span class="sxs-lookup"><span data-stu-id="50429-135">Under the heading **Specify the destination port number**, select **From this destination port or range**.</span></span> <span data-ttu-id="50429-136">Na caixa de texto acompanhada, digite o intervalo de porta reservado para transmissões de áudio.</span><span class="sxs-lookup"><span data-stu-id="50429-136">In the accompanying text box, type the port range reserved for audio transmissions.</span></span> <span data-ttu-id="50429-137">Por exemplo, se você reservou portas 49152 pelas portas 57500 para tráfego de áudio, insira o intervalo de porta usando este formato: **49152:57500**.</span><span class="sxs-lookup"><span data-stu-id="50429-137">For example, if you reserved ports 49152 through ports 57500 for audio traffic then enter the port range using this format: **49152:57500**.</span></span> <span data-ttu-id="50429-138">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="50429-138">Click **Finish**.</span></span>

<span data-ttu-id="50429-139">Depois de criar a política de QoS para o tráfego de áudio, você deve criar uma segunda política para o tráfego de vídeo.</span><span class="sxs-lookup"><span data-stu-id="50429-139">After you have created the QoS policy for audio traffic you should create a second policy for video traffic.</span></span> <span data-ttu-id="50429-140">Para criar uma política de vídeo, siga o mesmo procedimento básico que você seguiu ao criar a política de áudio, como fazer essas substituições:</span><span class="sxs-lookup"><span data-stu-id="50429-140">To create a policy for video, follow the same basic procedure you followed when creating the audio policy, making these substitutions:</span></span>

  - <span data-ttu-id="50429-141">Use um nome de política diferente (e exclusivo) (por exemplo, **vídeo do Lync Server**).</span><span class="sxs-lookup"><span data-stu-id="50429-141">Use a different (and unique) policy name (for example, **Lync Server Video**).</span></span>

  - <span data-ttu-id="50429-142">Defina o valor de DSCP para **34** em vez de 46.</span><span class="sxs-lookup"><span data-stu-id="50429-142">Set the DSCP value to **34** instead of 46.</span></span> <span data-ttu-id="50429-143">(Observe que você não precisa usar um valor de DSCP de 34.</span><span class="sxs-lookup"><span data-stu-id="50429-143">(Note that you do not have to use a DSCP value of 34.</span></span> <span data-ttu-id="50429-144">O único requisito é que você use um valor DSCP diferente para vídeo do que o usado para áudio.)</span><span class="sxs-lookup"><span data-stu-id="50429-144">The only requirement is that you use a different DSCP value for video than you used for audio.)</span></span>

  - <span data-ttu-id="50429-145">Use o intervalo de porta configurado anteriormente para o tráfego de vídeo.</span><span class="sxs-lookup"><span data-stu-id="50429-145">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="50429-146">Por exemplo, se você reservou portas de 57501 a 65535 para vídeo, defina o intervalo de porta como: **57501:65535**.</span><span class="sxs-lookup"><span data-stu-id="50429-146">For example, if you have reserved ports 57501 through 65535 for video, then set the port range to this: **57501:65535**.</span></span> <span data-ttu-id="50429-147">Novamente, isso deve ser configurado como o intervalo de porta de destino.</span><span class="sxs-lookup"><span data-stu-id="50429-147">Again, this should be configured as the destination port range.</span></span>

<span data-ttu-id="50429-148">Se você decidir criar uma política para gerenciar o tráfego de compartilhamento de aplicativos, será necessário criar uma terceira política e fazer as seguintes substituições:</span><span class="sxs-lookup"><span data-stu-id="50429-148">If you decide to create a policy for managing application sharing traffic you must create a third policy, making the following substitutions:</span></span>

  - <span data-ttu-id="50429-149">Use um nome de política diferente (e exclusivo) (por exemplo, **compartilhamento de aplicativos do Lync Server**).</span><span class="sxs-lookup"><span data-stu-id="50429-149">Use a different (and unique) policy name (for example, **Lync Server Application Sharing**).</span></span>

  - <span data-ttu-id="50429-150">Defina o valor de DSCP para **24** em vez de 46.</span><span class="sxs-lookup"><span data-stu-id="50429-150">Set the DSCP value to **24** instead of 46.</span></span> <span data-ttu-id="50429-151">(Novamente, você não precisa usar um valor de DSCP de 24.</span><span class="sxs-lookup"><span data-stu-id="50429-151">(Again, you do not have to use a DSCP value of 24.</span></span> <span data-ttu-id="50429-152">O único requisito é que você use um valor DSCP diferente para compartilhamento de aplicativos do que usou para áudio ou vídeo.)</span><span class="sxs-lookup"><span data-stu-id="50429-152">The only requirement is that you use a different DSCP value for application sharing than you used for audio or for video.)</span></span>

  - <span data-ttu-id="50429-153">Use o intervalo de porta configurado anteriormente para o tráfego de vídeo.</span><span class="sxs-lookup"><span data-stu-id="50429-153">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="50429-154">Por exemplo, se você reservou portas de 40803 a 49151 para compartilhamento de aplicativos, defina o intervalo de porta como: **40803:49151**.</span><span class="sxs-lookup"><span data-stu-id="50429-154">For example, if you have reserved ports 40803 through 49151 for application sharing, then set the port range to this: **40803:49151**.</span></span>

<span data-ttu-id="50429-155">As novas políticas que você criou não entrarão em vigor até que a política de grupo seja atualizada em seus servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="50429-155">The new policies you have created will not take effect until Group Policy has been refreshed on your Edge servers.</span></span> <span data-ttu-id="50429-156">Embora a Política de Grupo seja periodicamente atualizada por si só, você pode forçar a atualização imediata executando o comando a seguir em cada computador em que a Política de Grupo deve ser atualizada:</span><span class="sxs-lookup"><span data-stu-id="50429-156">Although Group Policy periodically refreshes on its own, you can force an immediate refresh by running the following command on each computer where Group Policy needs to be refreshed:</span></span>

    Gpudate.exe /force

<span data-ttu-id="50429-157">Esse comando pode ser executado no servidor do Lync ou em qualquer janela de comando que esteja em execução em credenciais de administrador.</span><span class="sxs-lookup"><span data-stu-id="50429-157">This command can be run from within the Lync Server or from any command window that is running under administrator credentials.</span></span> <span data-ttu-id="50429-158">Para executar uma janela de comando com credenciais de administrador, clique em **Iniciar**, clique com o botão direito do mouse em **Prompt de Comando** e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="50429-158">To run a command window under administrator credentials, click **Start**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span> <span data-ttu-id="50429-159">Observe que talvez seja necessário reiniciar o servidor de borda mesmo após a execução do Gpudate.exe.</span><span class="sxs-lookup"><span data-stu-id="50429-159">Note that you might need to restart the Edge server even after running Gpudate.exe.</span></span>

<span data-ttu-id="50429-160">Para ajudar a garantir que os pacotes de rede sejam marcados com o valor DSCP apropriado, você também deve criar uma nova entrada de registro em cada computador completando o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="50429-160">To help ensure that network packets are marked with the appropriate DSCP value, you should also create a new registry entry on each computer by completing the following procedure:</span></span>

1.  <span data-ttu-id="50429-161">Clique em **Iniciar** e em **executar**.</span><span class="sxs-lookup"><span data-stu-id="50429-161">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="50429-162">Na caixa de diálogo **executar** , digite **regedit** e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="50429-162">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="50429-163">No editor do registro, expanda **HKEY \_ local \_ Machine**, expanda **System**, expanda **CurrentControlSet**, expanda **Services** e, em seguida, expanda **tcpip**.</span><span class="sxs-lookup"><span data-stu-id="50429-163">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="50429-164">Clique com o botão direito do mouse em **tcpip**, aponte para **novo** e, em seguida, clique em **tecla**.</span><span class="sxs-lookup"><span data-stu-id="50429-164">Right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="50429-165">Após a criação da nova chave do registro, digite **QoS** e pressione ENTER para renomear a chave.</span><span class="sxs-lookup"><span data-stu-id="50429-165">After the new registry key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="50429-166">Clique com o botão direito do mouse em **QoS**, aponte para **novo** e clique em **valor da cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="50429-166">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="50429-167">Depois que o novo valor do registro for criado, digite não **use NLA** e pressione ENTER para renomear o valor.</span><span class="sxs-lookup"><span data-stu-id="50429-167">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="50429-168">Clique duas vezes em **não usar NLA**.</span><span class="sxs-lookup"><span data-stu-id="50429-168">Double-click **Do no use NLA**.</span></span> <span data-ttu-id="50429-169">Na caixa de diálogo **Editar Cadeia de caracteres** , digite **1** na caixa **dados do valor** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="50429-169">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

7.  <span data-ttu-id="50429-170">Feche o editor do registro e reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="50429-170">Close the Registry Editor and then reboot your computer.</span></span>

<span data-ttu-id="50429-171"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="50429-171"></div>

<span> </span>

</div>

</div>

</span></span></div>

