---
title: 'Lync Server 2013: Configurando políticas de qualidade de serviço para clientes em execução no Windows 7 ou no Windows 8'
description: 'Lync Server 2013: Configurando políticas de qualidade de serviço para clientes em execução no Windows 7 ou no Windows 8.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Quality of Service policies for clients running on Windows 7 or Windows 8
ms:assetid: efff2b98-b3fb-4183-a4f0-329a9105ce2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205371(v=OCS.15)
ms:contentKeyID: 48185785
ms.date: 03/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: faba5fc54ef73bfc738f94ee7209fc46a7cdc208
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432692"
---
# <a name="configuring-quality-of-service-policies-in-lync-server-2013-for-clients-running-on-windows-7-or-windows-8"></a><span data-ttu-id="08b91-103">Configurando políticas de qualidade de serviço no Lync Server 2013 para clientes em execução no Windows 7 ou no Windows 8</span><span class="sxs-lookup"><span data-stu-id="08b91-103">Configuring Quality of Service policies in Lync Server 2013 for clients running on Windows 7 or Windows 8</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="08b91-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="08b91-104">

<span> </span></span></span>

<span data-ttu-id="08b91-105">_**Tópico da última modificação:** 2016-03-29_</span><span class="sxs-lookup"><span data-stu-id="08b91-105">_**Topic Last Modified:** 2016-03-29_</span></span>

<span data-ttu-id="08b91-106">Além de especificar intervalos de porta para uso por seus clientes do Lync, você também deve criar políticas de qualidade de serviço separadas que serão aplicadas a computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="08b91-106">In addition to specifying port ranges for use by your Lync clients you must also create separate Quality of Service policies that will be applied to client computers.</span></span> <span data-ttu-id="08b91-107">(As políticas de qualidade de serviço criadas para servidores de conferência, aplicativos e remediação não devem ser aplicadas a computadores cliente.) Essas informações se aplicam apenas a computadores executando o cliente Lync 2013 e o Windows 7 ou Windows 8.</span><span class="sxs-lookup"><span data-stu-id="08b91-107">(The Quality of Service policies created for Conferencing, Application, and Mediation servers should not be applied to client computers.) This information applies only to computers running the Lync 2013 client and either Windows 7 or Windows 8.</span></span>

<span data-ttu-id="08b91-108">O exemplo a seguir usa esse conjunto de intervalos de porta para criar uma política de áudio e uma política de vídeo:</span><span class="sxs-lookup"><span data-stu-id="08b91-108">The following example uses this set of port ranges to create an audio policy and a video policy:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08b91-109">Tipo de tráfego do cliente</span><span class="sxs-lookup"><span data-stu-id="08b91-109">Client Traffic Type</span></span></th>
<th><span data-ttu-id="08b91-110">Início da porta</span><span class="sxs-lookup"><span data-stu-id="08b91-110">Port Start</span></span></th>
<th><span data-ttu-id="08b91-111">Intervalo de porta</span><span class="sxs-lookup"><span data-stu-id="08b91-111">Port Range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08b91-112">Áudio</span><span class="sxs-lookup"><span data-stu-id="08b91-112">Audio</span></span></p></td>
<td><p><span data-ttu-id="08b91-113">50020</span><span class="sxs-lookup"><span data-stu-id="08b91-113">50020</span></span></p></td>
<td><p><span data-ttu-id="08b91-114">cedido</span><span class="sxs-lookup"><span data-stu-id="08b91-114">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08b91-115">Vídeo</span><span class="sxs-lookup"><span data-stu-id="08b91-115">Video</span></span></p></td>
<td><p><span data-ttu-id="08b91-116">58000</span><span class="sxs-lookup"><span data-stu-id="08b91-116">58000</span></span></p></td>
<td><p><span data-ttu-id="08b91-117">cedido</span><span class="sxs-lookup"><span data-stu-id="08b91-117">20</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08b91-118">Compartilhamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="08b91-118">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="08b91-119">42000</span><span class="sxs-lookup"><span data-stu-id="08b91-119">42000</span></span></p></td>
<td><p><span data-ttu-id="08b91-120">cedido</span><span class="sxs-lookup"><span data-stu-id="08b91-120">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08b91-121">Transferência de arquivos</span><span class="sxs-lookup"><span data-stu-id="08b91-121">File transfer</span></span></p></td>
<td><p><span data-ttu-id="08b91-122">42020</span><span class="sxs-lookup"><span data-stu-id="08b91-122">42020</span></span></p></td>
<td><p><span data-ttu-id="08b91-123">cedido</span><span class="sxs-lookup"><span data-stu-id="08b91-123">20</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="08b91-124">Para criar uma política de áudio de qualidade de serviço para computadores com Windows 7 ou Windows 8, primeiro faça logon em um computador onde o gerenciamento de política de grupo foi instalado.</span><span class="sxs-lookup"><span data-stu-id="08b91-124">To create a Quality of Service audio policy for Windows 7 or Windows 8 computers, first log on to a computer where Group Policy Management has been installed.</span></span> <span data-ttu-id="08b91-125">Abra gerenciamento de política de grupo (clique em **Iniciar**, aponte para **Ferramentas administrativas** e clique em **Gerenciamento de política de grupo**) e, em seguida, conclua o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="08b91-125">Open Group Policy Management (click **Start**, point to **Administrative Tools**, and then click **Group Policy Management**) and then complete the following procedure:</span></span>

1.  <span data-ttu-id="08b91-126">No gerenciamento de política de grupo, localize o contêiner em que a nova política deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="08b91-126">In Group Policy Management, locate the container where the new policy should be created.</span></span> <span data-ttu-id="08b91-127">Por exemplo, se todos os seus computadores cliente estiverem localizados em uma UO chamada clientes, a nova política deve ser criada na UO do cliente.</span><span class="sxs-lookup"><span data-stu-id="08b91-127">For example, if all your client computers are located in an OU named Clients then the new policy should be created in the Client OU.</span></span>

2.  <span data-ttu-id="08b91-128">Clique com o botão direito do mouse no contêiner apropriado e, em seguida, clique em **criar um GPO neste domínio e vincule-o aqui**.</span><span class="sxs-lookup"><span data-stu-id="08b91-128">Right-click the appropriate container and then click **Create a GPO in this domain, and Link it here**.</span></span>

3.  <span data-ttu-id="08b91-129">Na caixa de diálogo **novo GPO** , digite um nome para o novo objeto de política de grupo na caixa **nome** (por exemplo, **áudio do Lync**) e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="08b91-129">In the **New GPO** dialog box, type a name for the new Group Policy object in the **Name** box (for example, **Lync Audio**) and then click **OK**.</span></span>

4.  <span data-ttu-id="08b91-130">Clique com o botão direito do mouse na política recém-criada e clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="08b91-130">Right-click the newly-created policy and then click **Edit**.</span></span>

5.  <span data-ttu-id="08b91-131">No editor de gerenciamento de política de grupo, expanda **configuração do computador**, expanda **políticas**, expanda **configurações do Windows**, clique com o botão direito do mouse em **QoS baseada em política** e clique em **criar nova política**.</span><span class="sxs-lookup"><span data-stu-id="08b91-131">In the Group Policy Management Editor, expand **Computer Configuration**, expand **Policies**, expand **Windows Settings**, right-click **Policy-based QoS**, and then click **Create new policy**.</span></span>

6.  <span data-ttu-id="08b91-132">Na caixa de diálogo **QoS baseada em política** , na página de abertura, digite um nome para a nova política (por exemplo, **áudio do Lync**) na caixa **nome** .</span><span class="sxs-lookup"><span data-stu-id="08b91-132">In the **Policy-based QoS** dialog box, on the opening page, type a name for the new policy (e.g., **Lync Audio**) in the **Name** box.</span></span> <span data-ttu-id="08b91-133">Selecione **especificar valor DSCP** e defina o valor como **46**.</span><span class="sxs-lookup"><span data-stu-id="08b91-133">Select **Specify DSCP Value** and set the value to **46**.</span></span> <span data-ttu-id="08b91-134">Deixe **especificar a taxa de aceleração de saída** desmarcada e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="08b91-134">Leave **Specify Outbound Throttle Rate** unselected, and then click **Next**.</span></span>

7. <span data-ttu-id="08b91-135">Na próxima página, selecione **apenas aplicativos com esse nome executável** e insira o nome **Lync.exe** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="08b91-135">On the next page, select **Only applications with this executable name** and enter the name **Lync.exe**, and then click **Next**.</span></span> <span data-ttu-id="08b91-136">Essa configuração instrui a política a priorizar somente o tráfego coincidente do cliente do Lync.</span><span class="sxs-lookup"><span data-stu-id="08b91-136">This setting instructs the policy to only prioritize matching traffic from the Lync client.</span></span>

8.  <span data-ttu-id="08b91-137">Na terceira página, verifique se **qualquer endereço IP de origem** e **qualquer endereço IP de destino** estão selecionados e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="08b91-137">On the third page, make sure that both **Any source IP address** and **Any destination IP address** are selected and then click **Next**.</span></span> <span data-ttu-id="08b91-138">Essas duas configurações garantem que os pacotes serão gerenciados independentemente de qual computador (endereço IP) enviou esses pacotes e qual computador (endereço IP) receberá esses pacotes.</span><span class="sxs-lookup"><span data-stu-id="08b91-138">These two settings ensure that packets will be managed regardless of which computer (IP address) sent those packets and which computer (IP address) will receive those packets.</span></span>

9.  <span data-ttu-id="08b91-139">Na página quatro, selecione **TCP e UDP** na lista **Selecione o protocolo que esta política de QoS se aplica à** lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="08b91-139">On page four, select **TCP and UDP** from the **Select the protocol this QoS policy applies to** dropdown list.</span></span> <span data-ttu-id="08b91-140">TCP (Transmission Control Protocol) e UDP (User Datagram Protocol) são os dois protocolos de rede mais comumente usados pelo Lync Server e seus aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="08b91-140">TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two networking protocols most-commonly used by Lync Server and its client applications.</span></span>

10. <span data-ttu-id="08b91-141">Em título, **especifique o número da porta de origem**, selecione uma **destas portas de origem ou intervalo**.</span><span class="sxs-lookup"><span data-stu-id="08b91-141">Under the heading **Specify the source port number**, select **From this source port or range**.</span></span> <span data-ttu-id="08b91-142">Na caixa de texto acompanhada, digite o intervalo de porta reservado para transmissões de áudio.</span><span class="sxs-lookup"><span data-stu-id="08b91-142">In the accompanying text box, type the port range reserved for audio transmissions.</span></span> <span data-ttu-id="08b91-143">Por exemplo, se você reservou portas 50020 pelas portas 50039 para tráfego de áudio, insira o intervalo de porta usando este formato: **50020:50039**.</span><span class="sxs-lookup"><span data-stu-id="08b91-143">For example, if you reserved ports 50020 through ports 50039 for audio traffic enter the port range using this format: **50020:50039**.</span></span> <span data-ttu-id="08b91-144">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="08b91-144">Click **Finish**.</span></span>

<span data-ttu-id="08b91-145">Depois de criar a política de QoS para o áudio, você deve criar uma segunda política para vídeo.</span><span class="sxs-lookup"><span data-stu-id="08b91-145">After you have created the QoS policy for audio you should then create a second policy for video.</span></span> <span data-ttu-id="08b91-146">Para criar uma política de vídeo, siga o mesmo procedimento básico que você seguiu ao criar a política de áudio, como fazer essas substituições:</span><span class="sxs-lookup"><span data-stu-id="08b91-146">To create a policy for video, follow the same basic procedure you followed when creating the audio policy, making these substitutions:</span></span>

  - <span data-ttu-id="08b91-147">Use um nome de política diferente (e exclusivo) (por exemplo, **vídeo do Lync**).</span><span class="sxs-lookup"><span data-stu-id="08b91-147">Use a different (and unique) policy name (for example, **Lync Video**).</span></span>

  - <span data-ttu-id="08b91-148">Defina o valor de DSCP para **34** em vez de 46.</span><span class="sxs-lookup"><span data-stu-id="08b91-148">Set the DSCP value to **34** instead of 46.</span></span> <span data-ttu-id="08b91-149">(Conforme observado anteriormente, você não precisa usar o valor de DSCP 34; basta atribuir um valor de DSCP diferente do usado para áudio.)</span><span class="sxs-lookup"><span data-stu-id="08b91-149">(As noted previously, you do not have to use the DSCP value 34; you simply must assign a different DSCP value than the one used for audio.)</span></span>

  - <span data-ttu-id="08b91-150">Use o intervalo de porta configurado anteriormente para o tráfego de vídeo.</span><span class="sxs-lookup"><span data-stu-id="08b91-150">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="08b91-151">Por exemplo, se você reservou portas de 58000 a 58019 para vídeo, defina o intervalo de porta como: **58000:58019**.</span><span class="sxs-lookup"><span data-stu-id="08b91-151">For example, if you have reserved ports 58000 through 58019 for video, then set the port range to this: **58000:58019**.</span></span>

<span data-ttu-id="08b91-152">Se você decidir criar uma política para gerenciar o tráfego de compartilhamento de aplicativos, faça estas substituições:</span><span class="sxs-lookup"><span data-stu-id="08b91-152">If you decide to create a policy for managing application sharing traffic make these substitutions:</span></span>

  - <span data-ttu-id="08b91-153">Use um nome de política diferente (e exclusivo) (por exemplo, **compartilhamento de aplicativos do Lync Server**).</span><span class="sxs-lookup"><span data-stu-id="08b91-153">Use a different (and unique) policy name (for example, **Lync Server Application Sharing**).</span></span>

  - <span data-ttu-id="08b91-154">Defina o valor de DSCP para **24** em vez de 46.</span><span class="sxs-lookup"><span data-stu-id="08b91-154">Set the DSCP value to **24** instead of 46.</span></span> <span data-ttu-id="08b91-155">(Novamente, esse valor não precisa ser 24; ele simplesmente deve ser diferente dos valores de DSCP usados para áudio e vídeo.)</span><span class="sxs-lookup"><span data-stu-id="08b91-155">(Again, this value does not have to be 24; it simply must be different than the DSCP values used for audio and for video.)</span></span>

  - <span data-ttu-id="08b91-156">Use o intervalo de porta configurado anteriormente para o tráfego de vídeo.</span><span class="sxs-lookup"><span data-stu-id="08b91-156">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="08b91-157">Por exemplo, se você reservou portas de 42000 a 42019 para compartilhamento de aplicativos, defina o intervalo de porta como: **42000:42019**.</span><span class="sxs-lookup"><span data-stu-id="08b91-157">For example, if you have reserved ports 42000 through 42019 for application sharing, then set the port range to this: **42000:42019**.</span></span>

<span data-ttu-id="08b91-158">Para uma política de transferência de arquivos:</span><span class="sxs-lookup"><span data-stu-id="08b91-158">For a file transfer policy:</span></span>

  - <span data-ttu-id="08b91-159">Use um nome de política diferente (e exclusivo) (por exemplo, **transferências de arquivo do Lync Server**).</span><span class="sxs-lookup"><span data-stu-id="08b91-159">Use a different (and unique) policy name (for example, **Lync Server File Transfers**).</span></span>

  - <span data-ttu-id="08b91-160">Defina o valor de DSCP para **14**.</span><span class="sxs-lookup"><span data-stu-id="08b91-160">Set the DSCP value to **14**.</span></span> <span data-ttu-id="08b91-161">(Novamente, esse valor não precisa ser 14; ele simplesmente deve ser um código DSCP exclusivo.)</span><span class="sxs-lookup"><span data-stu-id="08b91-161">(Again, this value does not have to be 14; it simply must be a unique DSCP code.)</span></span>

  - <span data-ttu-id="08b91-162">Use o intervalo de porta configurado anteriormente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="08b91-162">Use the previously-configured port range for application.</span></span> <span data-ttu-id="08b91-163">Por exemplo, se você reservou portas de 42020 a 42039 para compartilhamento de aplicativos, defina o intervalo de porta como: **42020:42039**.</span><span class="sxs-lookup"><span data-stu-id="08b91-163">For example, if you have reserved ports 42020 through 42039 for application sharing, then set the port range to this: **42020:42039**.</span></span>

<span data-ttu-id="08b91-164">As novas políticas que você criou não entrarão em vigor até que a política de grupo seja atualizada em seus computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="08b91-164">The new policies you have created will not take effect until Group Policy has been refreshed on your client computers.</span></span> <span data-ttu-id="08b91-165">Embora a Política de Grupo seja periodicamente atualizada por si só, você pode forçar a atualização imediata executando o comando a seguir em cada computador em que a Política de Grupo deve ser atualizada:</span><span class="sxs-lookup"><span data-stu-id="08b91-165">Although Group Policy periodically refreshes on its own, you can force an immediate refresh by running the following command on each computer where Group Policy needs to be refreshed:</span></span>

    Gpudate.exe /force

<span data-ttu-id="08b91-166">Esse comando pode ser executado em qualquer janela de comando executada com credenciais de administrador.</span><span class="sxs-lookup"><span data-stu-id="08b91-166">This command can be run from any command window that is running under administrator credentials.</span></span> <span data-ttu-id="08b91-167">Para executar uma janela de comando com credenciais de administrador, clique em **Iniciar**, clique com o botão direito do mouse em **Prompt de Comando** e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="08b91-167">To run a command window under administrator credentials, click **Start**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

<span data-ttu-id="08b91-168">Lembre-se de que essas políticas devem ser direcionadas para seus computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="08b91-168">Keep in mind that these policies should be targeted towards your client computers.</span></span> <span data-ttu-id="08b91-169">Elas não devem ser aplicadas a servidores que executam o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="08b91-169">They should not be applied to servers running Lync Server.</span></span>

<span data-ttu-id="08b91-170">Para ajudar a garantir que os pacotes de rede sejam marcados com o valor DSCP apropriado, você também deve criar uma nova entrada de registro em cada computador completando o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="08b91-170">To help ensure that network packets are marked with the appropriate DSCP value, you should also create a new registry entry on each computer by completing the following procedure:</span></span>

1.  <span data-ttu-id="08b91-171">Clique em **Iniciar** e em **executar**.</span><span class="sxs-lookup"><span data-stu-id="08b91-171">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="08b91-172">Na caixa de diálogo **executar** , digite **regedit** e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="08b91-172">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="08b91-173">No editor do registro, expanda **HKEY \_ local \_ Machine**, expanda **System**, expanda **CurrentControlSet**, expanda **Services** e, em seguida, expanda **tcpip**.</span><span class="sxs-lookup"><span data-stu-id="08b91-173">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="08b91-174">Clique com o botão direito do mouse em **tcpip**, aponte para **novo** e, em seguida, clique em **tecla**.</span><span class="sxs-lookup"><span data-stu-id="08b91-174">Right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="08b91-175">Após a criação da nova chave do registro, digite **QoS** e pressione ENTER para renomear a chave.</span><span class="sxs-lookup"><span data-stu-id="08b91-175">After the new registry key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="08b91-176">Clique com o botão direito do mouse em **QoS**, aponte para **novo** e clique em **valor da cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="08b91-176">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="08b91-177">Depois que o novo valor do registro for criado, digite não **use NLA** e pressione ENTER para renomear o valor.</span><span class="sxs-lookup"><span data-stu-id="08b91-177">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="08b91-178">Clique duas vezes em **não usar NLA**.</span><span class="sxs-lookup"><span data-stu-id="08b91-178">Double-click **Do not use NLA**.</span></span> <span data-ttu-id="08b91-179">Na caixa de diálogo **Editar Cadeia de caracteres** , digite **1** na caixa **dados do valor** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="08b91-179">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

7.  <span data-ttu-id="08b91-180">Feche o editor do registro e reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="08b91-180">Close the Registry Editor and then reboot your computer.</span></span>

<div>

## <a name="configuring-quality-of-service-on-computers-with-multiple-network-adapters"></a><span data-ttu-id="08b91-181">Configurando a qualidade do serviço em computadores com vários adaptadores de rede</span><span class="sxs-lookup"><span data-stu-id="08b91-181">Configuring Quality of Service on Computers with Multiple Network Adapters</span></span>

<span data-ttu-id="08b91-182">Se você tiver um computador com vários adaptadores de rede, ocasionalmente poderá ter problemas nos quais valores de DSCP são mostrados como 0x00, em vez do valor configurado.</span><span class="sxs-lookup"><span data-stu-id="08b91-182">If you have a computer that has multiple network adapters you might occasionally run into issues where DSCP values are shown as 0x00 rather than the configured value.</span></span> <span data-ttu-id="08b91-183">Isso normalmente ocorrerá em computadores em que um ou mais adaptadores de rede não conseguem acessar o domínio do Active Directory (por exemplo, se esses adaptadores forem usados para uma rede privada).</span><span class="sxs-lookup"><span data-stu-id="08b91-183">This will typically occur on computers where one or more of the network adapters are not able to access your Active Directory domain (for example, if these adapters are used for a private network).</span></span> <span data-ttu-id="08b91-184">Em casos como esse, os valores de DSCP serão marcados para os adaptadores que podem acessar o domínio, mas não serão marcados para adaptadores que não podem acessar o domínio.</span><span class="sxs-lookup"><span data-stu-id="08b91-184">In cases like that, DSCP values will be tagged for the adapters that can access the domain, but will not be tagged for adapters that cannot access the domain.</span></span>

<span data-ttu-id="08b91-185">Se você quiser marcar valores DSCP para todos os adaptadores de rede em um computador, incluindo adaptadores que não têm acesso ao seu domínio, será necessário adicionar e configurar um valor para o registro.</span><span class="sxs-lookup"><span data-stu-id="08b91-185">If you would like to tag DSCP values for all the network adapters in a computer, including adapters that do not have access to your domain, then you will need to add and configure a value to the registry.</span></span> <span data-ttu-id="08b91-186">Isso pode ser feito completando o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="08b91-186">That can be done by completing the following procedure:</span></span>

1.  <span data-ttu-id="08b91-187">Clique em **Iniciar** e em **executar**.</span><span class="sxs-lookup"><span data-stu-id="08b91-187">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="08b91-188">Na caixa de diálogo **executar** , digite **regedit** e pressione Enter.</span><span class="sxs-lookup"><span data-stu-id="08b91-188">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="08b91-189">No editor do registro, expanda **HKEY \_ local \_ Machine**, expanda **System**, expanda **CurrentControlSet**, expanda **Services** e, em seguida, expanda **tcpip**.</span><span class="sxs-lookup"><span data-stu-id="08b91-189">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="08b91-190">Se você não vir uma chave do registro rotulada como **QoS** , clique com o botão direito do mouse em **tcpip**, aponte para **novo** e clique em **tecla**.</span><span class="sxs-lookup"><span data-stu-id="08b91-190">If you do not see a registry key labeled **QoS** then right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="08b91-191">Após a criação da nova chave, digite **QoS** e pressione ENTER para renomear a chave.</span><span class="sxs-lookup"><span data-stu-id="08b91-191">After the new key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="08b91-192">Clique com o botão direito do mouse em **QoS**, aponte para **novo** e clique em **valor da cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="08b91-192">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="08b91-193">Depois que o novo valor do registro for criado, digite não **use NLA** e pressione ENTER para renomear o valor.</span><span class="sxs-lookup"><span data-stu-id="08b91-193">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="08b91-194">Clique duas vezes em **não usar NLA**.</span><span class="sxs-lookup"><span data-stu-id="08b91-194">Double-click **Do not use NLA**.</span></span> <span data-ttu-id="08b91-195">Na caixa de diálogo **Editar Cadeia de caracteres** , digite **1** na caixa **dados do valor** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="08b91-195">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

<span data-ttu-id="08b91-196">Depois de criar e configurar o novo valor do registro, você precisará reinicializar o computador para que as alterações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="08b91-196">After creating and configuring the new registry value you will need to reboot your computer in order for the changes to take effect.</span></span>

<span data-ttu-id="08b91-197"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="08b91-197"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

