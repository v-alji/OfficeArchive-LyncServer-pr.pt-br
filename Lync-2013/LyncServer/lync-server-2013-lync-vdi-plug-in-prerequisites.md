---
title: 'Lync Server 2013: Pré-requisitos do plug-in Lync VDI'
description: 'Lync Server 2013: pré-requisitos de plug-in VDI do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync VDI plug-in prerequisites
ms:assetid: da25a976-7624-4dfc-b332-9c4db4ee78da
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205304(v=OCS.15)
ms:contentKeyID: 48185552
ms.date: 03/07/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4389f776747426d07442e29418ab97e9609de7ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426239"
---
# <a name="lync-vdi-plug-in-prerequisites-in-lync-server-2013"></a><span data-ttu-id="87119-103">Pré-requisitos do plug-in Lync VDI no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="87119-103">Lync VDI plug-in prerequisites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="87119-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="87119-104">

<span> </span></span></span>

<span data-ttu-id="87119-105">_**Tópico da última modificação:** 2017-03-07_</span><span class="sxs-lookup"><span data-stu-id="87119-105">_**Topic Last Modified:** 2017-03-07_</span></span>

<span data-ttu-id="87119-106">Em um ambiente da Virtual Desktop Infrastructure (VDI), as máquinas virtuais e o computador local do usuário devem atender aos requisitos descritos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="87119-106">In a virtual desktop infrastructure (VDI) environment, the virtual machines and the user’s local computer must meet the requirements outlined in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="87119-107">Consulte seu provedor de soluções de virtualização para obter detalhes sobre como instalar e implantar o ambiente virtualizado.</span><span class="sxs-lookup"><span data-stu-id="87119-107">Refer to your virtualization solution provider for details about how to install and deploy the virtualized environment.</span></span> <span data-ttu-id="87119-108">Para obter informações sobre como implantar um ambiente virtualizado com base no Hyper-V e nos serviços de área de trabalho remota, consulte os seguintes artigos na biblioteca do Microsoft TechNet:</span><span class="sxs-lookup"><span data-stu-id="87119-108">For information about deploying a virtualized environment based on Hyper-V and Remote Desktop Services, see the following articles in the Microsoft TechNet Library:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="87119-109">Hyper-V em <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247514">https://go.microsoft.com/fwlink/p/?linkid=247514</A></span><span class="sxs-lookup"><span data-stu-id="87119-109">Hyper-V at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247514">https://go.microsoft.com/fwlink/p/?linkid=247514</A></span></span></P>
> <LI>
> <P><span data-ttu-id="87119-110">Serviços de área de trabalho remota no Windows Server &nbsp; 2008 &nbsp; R2 em <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247513">https://go.microsoft.com/fwlink/p/?linkid=247513</A></span><span class="sxs-lookup"><span data-stu-id="87119-110">Remote Desktop Services in Windows Server&nbsp;2008&nbsp;R2 at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=247513">https://go.microsoft.com/fwlink/p/?linkid=247513</A></span></span></P></LI></UL>



</div>

<span data-ttu-id="87119-111">Veja a seguir os requisitos para as máquinas virtuais em execução no computador do Data Center:</span><span class="sxs-lookup"><span data-stu-id="87119-111">The following are requirements for the virtual machines running on the data center computer:</span></span>

  - <span data-ttu-id="87119-112">Máquinas virtuais devem ser configuradas com o Windows 10, o Windows 8,1, o Windows 8, o Windows 7 ou o Windows Server 2008 R2 com os service packs mais recentes.</span><span class="sxs-lookup"><span data-stu-id="87119-112">Virtual machines must be configured with Windows 10, Windows 8.1, Windows 8, Windows 7, or Windows Server 2008 R2 with the latest service packs.</span></span>

<span data-ttu-id="87119-113">Veja a seguir os requisitos para o usuário e o computador local do usuário:</span><span class="sxs-lookup"><span data-stu-id="87119-113">The following are requirements for the user and the user’s local computer:</span></span>

  - <span data-ttu-id="87119-114">O usuário deve ser hospedado no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="87119-114">The user must be homed on Lync Server 2013.</span></span>

  - <span data-ttu-id="87119-115">O computador local deve estar executando o Windows Embedded Standard 7 com SP1, o Windows 7 com SP1, o Windows 8, o Windows 8,1 Embedded ou o Windows 8,1 (não incorporado).</span><span class="sxs-lookup"><span data-stu-id="87119-115">The local computer must be running Windows Embedded Standard 7 with SP1, Windows 7 with SP1, Windows 8, Windows 8.1 Embedded, or Windows 8.1 (not embedded).</span></span>

  - <span data-ttu-id="87119-116">Se você estiver usando os serviços de área de trabalho remota, o bit de bits de plug-in do Lync da VDI (ou seja, se o aplicativo for 32 bits ou 64 bits) deve corresponder ao sistema operacional do sistema operacional do computador local.</span><span class="sxs-lookup"><span data-stu-id="87119-116">If you are using Remote Desktop Services, the Lync VDI plug-in bitness (that is, whether the application is 32-bit or 64-bit) must match the local computer’s operating system bitness.</span></span> <span data-ttu-id="87119-117">A bits do sistema operacional no computador local e o sistema operacional na máquina virtual não precisam ser correspondentes.</span><span class="sxs-lookup"><span data-stu-id="87119-117">The bitness of the operating system on the local computer and the operating system on the virtual machine do not need to match.</span></span> <span data-ttu-id="87119-118">Se você estiver usando outra solução ou plataforma de virtualização, consulte a orientação de seu provedor de soluções de virtualização sobre requisitos de bits.</span><span class="sxs-lookup"><span data-stu-id="87119-118">If you are using another virtualization solution or platform, refer to guidance from your virtualization solution provider about bitness requirements.</span></span>

  - <span data-ttu-id="87119-119">O computador local deve estar executando a versão mais recente do cliente da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="87119-119">The local computer must be running the latest version of the remote desktop client.</span></span> <span data-ttu-id="87119-120">Instale as últimas atualizações do cliente de Serviços de Área de Trabalho Remota da Microsoft ou o software cliente de área de trabalho remota mais recente do seu provedor de soluções de virtualização.</span><span class="sxs-lookup"><span data-stu-id="87119-120">Install the latest updates of Remote Desktop Services client from Microsoft or the latest remote desktop client software from your virtualization solution provider.</span></span> <span data-ttu-id="87119-121">Para obter as atualizações mais recentes dos serviços de área de trabalho remota, consulte [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032) .</span><span class="sxs-lookup"><span data-stu-id="87119-121">For the latest Remote Desktop Services updates, see [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032).</span></span>

  - <span data-ttu-id="87119-122">No computador local, as configurações do cliente de área de trabalho remota devem ser definidas para que o áudio seja reproduzido no computador local e a gravação remota seja desabilitada.</span><span class="sxs-lookup"><span data-stu-id="87119-122">On the local computer, the remote desktop client settings must be configured so that audio plays on the local computer and remote recording is disabled.</span></span> <span data-ttu-id="87119-123">Para definir essas configurações para a conexão de área de trabalho remota no Windows, consulte a próxima seção, "para definir as configurações de conexão de área de trabalho remota".</span><span class="sxs-lookup"><span data-stu-id="87119-123">To configure these settings for Remote Desktop Connection in Windows, see the next section, "To configure Remote Desktop Connection settings."</span></span>

<div>

## <a name="to-configure-remote-desktop-connection-settings"></a><span data-ttu-id="87119-124">Para definir as configurações da conexão de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="87119-124">To configure Remote Desktop Connection settings</span></span>

<span data-ttu-id="87119-125">Para preparar a conexão de área de trabalho remota no Windows para o plug-in VDI do Lync, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="87119-125">To prepare Remote Desktop Connection in Windows for the Lync VDI plug-in, follow these steps.</span></span>

1.  <span data-ttu-id="87119-126">Se o computador local estiver executando o Windows 8, pule esta etapa.</span><span class="sxs-lookup"><span data-stu-id="87119-126">If the local computer is running Windows 8, skip this step.</span></span> <span data-ttu-id="87119-127">Se o computador local estiver executando o Windows 7 com SP1, instale a versão mais recente do Windows 8 do cliente dos serviços de área de trabalho remota, disponível em [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032) .</span><span class="sxs-lookup"><span data-stu-id="87119-127">If the local computer is running Windows 7 with SP1, install the latest Windows 8 version of the Remote Desktop Services client, available at [https://go.microsoft.com/fwlink/p/?LinkId=268032](https://go.microsoft.com/fwlink/p/?linkid=268032).</span></span>

2.  <span data-ttu-id="87119-128">Inicie o cliente de Serviços de Área de Trabalho Remota clicando em **Iniciar** e em **Conexão de Área de Trabalho Remota**.</span><span class="sxs-lookup"><span data-stu-id="87119-128">Start the Remote Desktop Services client by clicking **Start**, and then clicking **Remote Desktop Connection**.</span></span>

3.  <span data-ttu-id="87119-129">Clique em **Opções**.</span><span class="sxs-lookup"><span data-stu-id="87119-129">Click **Options**.</span></span>

4.  <span data-ttu-id="87119-130">Clique na guia **Recursos Locais**. Em **Áudio remoto**, clique em **Configurações** e faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="87119-130">Click the **Local Resources** tab. Under **Remote audio**, click **Settings**, and then do the following:</span></span>
    
      - <span data-ttu-id="87119-131">Em **Reprodução de áudio remoto**, selecione **Reproduzir neste computador**.</span><span class="sxs-lookup"><span data-stu-id="87119-131">Under **Remote audio playback**, select **Play on this computer**.</span></span>
    
      - <span data-ttu-id="87119-132">Em **Gravação de áudio remoto**, selecione **Não gravar**.</span><span class="sxs-lookup"><span data-stu-id="87119-132">Under **Remote audio recording**, select **Do not record**.</span></span>
    
      - <span data-ttu-id="87119-133">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="87119-133">Click **OK**.</span></span>

5.  <span data-ttu-id="87119-134">Clique na guia **Experiência**. Em **Desempenho**, desmarque a caixa de seleção **Armazenamento persistente de bitmaps em cache**.</span><span class="sxs-lookup"><span data-stu-id="87119-134">Click the **Experience** tab. Under **Performance**, clear the **Persistent bitmap caching** check box.</span></span>

6.  <span data-ttu-id="87119-135">Clique na guia **geral** . Em **computador**, digite o nome da máquina virtual e, em seguida, clique em **conectar**.</span><span class="sxs-lookup"><span data-stu-id="87119-135">Click the **General** tab. In **Computer**, type the name of the virtual machine, and then click **Connect**.</span></span>

<span data-ttu-id="87119-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="87119-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

