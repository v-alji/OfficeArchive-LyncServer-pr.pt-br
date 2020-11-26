---
title: 'Lync Server 2013: ferramenta de diagnóstico de chamadas do Lync'
description: 'Lync Server 2013: ferramenta de diagnóstico de chamadas do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync PreCall Diagnostics Tool
ms:assetid: 0ff291ec-cfb4-43eb-b5d6-a7a325681e3f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn451255(v=OCS.15)
ms:contentKeyID: 56708404
ms.date: 11/04/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17c2c51551fe0991eb354a628b1d4660baa1532b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426314"
---
# <a name="lync-precall-diagnostics-tool-in-lync-server-2013"></a><span data-ttu-id="ee3e7-103">Ferramenta de diagnóstico de chamadas do Lync no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee3e7-103">Lync PreCall Diagnostics Tool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee3e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee3e7-104">

<span> </span></span></span>

<span data-ttu-id="ee3e7-105">_**Tópico da última modificação:** 2016-11-04_</span><span class="sxs-lookup"><span data-stu-id="ee3e7-105">_**Topic Last Modified:** 2016-11-04_</span></span>

<span data-ttu-id="ee3e7-106">A ferramenta de diagnóstico de chamadas (PCD) do Lync é um aplicativo baseado em cliente que permite que você veja como o estado atual da sua rede pode afetar a qualidade de áudio em uma próxima chamada de voz empresarial.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-106">The Lync PreCall Diagnostics Tool (PCD) is a client-based application that allows you to see how the current state of your network might impact the audio quality in an upcoming Enterprise Voice call.</span></span>

<span data-ttu-id="ee3e7-107">O PCD é mais útil em situações em que o último nó de uma rede é provavelmente o mais fraco (por exemplo, com laptops em uma rede WiFi pública ou em usuários domésticos).</span><span class="sxs-lookup"><span data-stu-id="ee3e7-107">PCD is most useful in situations where the last hop of a network is likely to be the weakest (for example, with laptops on a public WiFi network or home users).</span></span> <span data-ttu-id="ee3e7-108">O PCD cria um fluxo de pacotes pequeno que atravessa o trecho final da rede.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-108">PCD creates a small packet stream that traverses this final leg of the network.</span></span> <span data-ttu-id="ee3e7-109">Em seguida, a ferramenta analisa o fluxo do pacote para estimar como a tremulação e a perda nesse segmento podem afetar a qualidade da chamada e, em seguida, fornecer um relatório.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-109">The tool then analyzes the packet stream to estimate how the jitter and loss along this leg might impact call quality, and then provides a report.</span></span> <span data-ttu-id="ee3e7-110">Você pode executar o PCD continuamente no cliente, mesmo quando as chamadas estiverem sendo feitas.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-110">You can run PCD continuously on the client, even while calls are being placed.</span></span> <span data-ttu-id="ee3e7-111">O fluxo do pacote não tem um efeito significativo na largura de banda.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-111">The packet stream does not have a significant effect on bandwidth.</span></span>

<span data-ttu-id="ee3e7-112">**A versão mais recente do PCD, versão 1,1, inclui os seguintes aprimoramentos:**</span><span class="sxs-lookup"><span data-stu-id="ee3e7-112">**The latest release of the PCD, version 1.1, includes the following enhancements:**</span></span>

  - <span data-ttu-id="ee3e7-113">Suporte para senhas mais longas, que agora podem ter até 127 caracteres</span><span class="sxs-lookup"><span data-stu-id="ee3e7-113">Support for longer passwords, which can now be up to 127 characters</span></span>

  - <span data-ttu-id="ee3e7-114">Diagnósticos adicionais para problemas de entrada de autenticação</span><span class="sxs-lookup"><span data-stu-id="ee3e7-114">Additional diagnostics for authentication sign-in issues</span></span>

  - <span data-ttu-id="ee3e7-115">Melhor suporte para implantações híbridas do Lync</span><span class="sxs-lookup"><span data-stu-id="ee3e7-115">Better support for Lync hybrid deployments</span></span>

  - <span data-ttu-id="ee3e7-116">Atualizações do seletor de credenciais</span><span class="sxs-lookup"><span data-stu-id="ee3e7-116">Updates to credential picker</span></span>

  - <span data-ttu-id="ee3e7-117">Melhorias de estabilidade</span><span class="sxs-lookup"><span data-stu-id="ee3e7-117">Stability improvements</span></span>

<span data-ttu-id="ee3e7-118">Agradecemos qualquer feedback.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-118">We appreciate any feedback.</span></span> <span data-ttu-id="ee3e7-119">Envie todas as perguntas ou problemas de suporte ao alias de [comentários do PCD](mailto:pcdfb@microsoft.com) em <pcdfb@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="ee3e7-119">Please send all support questions or issues to the [PCD Feedback](mailto:pcdfb@microsoft.com) alias at <pcdfb@microsoft.com>.</span></span>

<span data-ttu-id="ee3e7-120">Este tópico inclui as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="ee3e7-120">This topic includes the following sections:</span></span>

  - <span data-ttu-id="ee3e7-121">Versões do Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ee3e7-121">Lync PCD Versions</span></span>

  - <span data-ttu-id="ee3e7-122">Requisitos do sistema do Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ee3e7-122">Lync PCD System Requirements</span></span>

  - <span data-ttu-id="ee3e7-123">Recursos do Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ee3e7-123">Lync PCD Features</span></span>

  - <span data-ttu-id="ee3e7-124">Executando o Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ee3e7-124">Running Lync PCD</span></span>

  - <span data-ttu-id="ee3e7-125">Desinstalar o Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ee3e7-125">Uninstalling Lync PCD</span></span>

<span id="Version"></span>

<div>

## <a name="lync-pcd-versions"></a><span data-ttu-id="ee3e7-126">Versões do Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ee3e7-126">Lync PCD Versions</span></span>

<span data-ttu-id="ee3e7-127">Este tópico descreve as seguintes versões da ferramenta, disponível para download gratuito:</span><span class="sxs-lookup"><span data-stu-id="ee3e7-127">This topic describes the following versions of the tool, available for free download:</span></span>

  - <span data-ttu-id="ee3e7-128">Aplicativo da área de trabalho do Windows ( [https://go.microsoft.com/fwlink/?LinkId=327914](https://go.microsoft.com/fwlink/p/?linkid=327914) )</span><span class="sxs-lookup"><span data-stu-id="ee3e7-128">Windows Desktop App ([https://go.microsoft.com/fwlink/?LinkId=327914](https://go.microsoft.com/fwlink/p/?linkid=327914))</span></span>

</div>

<span id="Requirements"></span>

<div>

## <a name="lync-pcd-system-requirements"></a><span data-ttu-id="ee3e7-129">Requisitos do sistema do Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ee3e7-129">Lync PCD System Requirements</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ee3e7-130">O PCD requer que a API da Web de comunicação unificada (UCWA) seja instalada e configurada para dar suporte a clientes móveis na implantação do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-130">PCD requires that Unified Communications Web API (UCWA) be installed and configured to support mobile clients in the Lync Server deployment.</span></span> <span data-ttu-id="ee3e7-131">O UCWA é instalado com o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-131">UCWA is installed with Lync Server.</span></span>



</div>

<div>

## <a name="windows-desktop-app-requirements"></a><span data-ttu-id="ee3e7-132">Requisitos do aplicativo da área de trabalho do Windows</span><span class="sxs-lookup"><span data-stu-id="ee3e7-132">Windows Desktop App Requirements</span></span>

  - <span data-ttu-id="ee3e7-133">Qualquer edição do sistema operacional Windows 7 ou Windows 8</span><span class="sxs-lookup"><span data-stu-id="ee3e7-133">Any edition of the Windows 7 or Windows 8 operating system</span></span>

  - <span data-ttu-id="ee3e7-134">Microsoft .NET Framework 4,5 disponível em [https://go.microsoft.com/fwlink/?LinkId=327790](https://go.microsoft.com/fwlink/p/?linkid=327790)</span><span class="sxs-lookup"><span data-stu-id="ee3e7-134">Microsoft .NET Framework 4.5 available at [https://go.microsoft.com/fwlink/?LinkId=327790](https://go.microsoft.com/fwlink/p/?linkid=327790)</span></span>

</div>

</div>

<span id="features"></span>

<div>

## <a name="lync-pcd-features"></a><span data-ttu-id="ee3e7-135">Recursos do Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ee3e7-135">Lync PCD Features</span></span>

<span data-ttu-id="ee3e7-136">O Lync PCD inclui os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="ee3e7-136">Lync PCD includes the following features:</span></span>

  - <span data-ttu-id="ee3e7-137">Executar no padrão sob demanda (intermitências de 2 minutos)</span><span class="sxs-lookup"><span data-stu-id="ee3e7-137">Run in default On Demand (2 minute bursts)</span></span>

  - <span data-ttu-id="ee3e7-138">Executar em modo (até 24 horas no modo de exibição ajustado)</span><span class="sxs-lookup"><span data-stu-id="ee3e7-138">Run in Always On (up to 24 hours in snapped view) mode</span></span>

  - <span data-ttu-id="ee3e7-139">Modo de exibição histórico de suas execuções de teste</span><span class="sxs-lookup"><span data-stu-id="ee3e7-139">Historical view of your test runs</span></span>

  - <span data-ttu-id="ee3e7-140">Diagnosticar falhas de entrada (somente Lync PCD para Windows 8)</span><span class="sxs-lookup"><span data-stu-id="ee3e7-140">Diagnose sign-in failures (Lync PCD for Windows 8 only)</span></span>

<span data-ttu-id="ee3e7-141">![Captura de tela de progresso do recurso de entrada do Lync PCD](images/Dn451255.7e0eb891-1481-47ae-8d63-164468f69c96(OCS.15).png "Captura de tela de progresso do recurso de entrada do Lync PCD")</span><span class="sxs-lookup"><span data-stu-id="ee3e7-141">![Lync PCD features Sign in progress screen shot](images/Dn451255.7e0eb891-1481-47ae-8d63-164468f69c96(OCS.15).png "Lync PCD features Sign in progress screen shot")</span></span>

  - <span data-ttu-id="ee3e7-142">Modo de exibição gráfico de métricas de rede – MOS de rede, perda de pacotes e Tremulação de interentrada em tela cheia e exibição ajustada.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-142">Graphical view of network metrics – Network MOS, Packet Loss and Interarrival Jitter in full screen and snapped view.</span></span>

<span data-ttu-id="ee3e7-143">**Modo de exibição de tela inteira**</span><span class="sxs-lookup"><span data-stu-id="ee3e7-143">**Full screen view**</span></span>

<span data-ttu-id="ee3e7-144">![Gráficos de resultado de teste da ferramenta de diagnóstico de chamada](images/Dn451255.5d01fd94-9e59-4823-96c7-7a1c83dd7d31(OCS.15).png "Gráficos de resultado de teste da ferramenta de diagnóstico de chamada")</span><span class="sxs-lookup"><span data-stu-id="ee3e7-144">![PreCall Diagnostic Tool test result graphs](images/Dn451255.5d01fd94-9e59-4823-96c7-7a1c83dd7d31(OCS.15).png "PreCall Diagnostic Tool test result graphs")</span></span>

<span data-ttu-id="ee3e7-145">**Modo de exibição ajustado**</span><span class="sxs-lookup"><span data-stu-id="ee3e7-145">**Snapped view**</span></span>

<span data-ttu-id="ee3e7-146">![Resultados do teste de utilização da ferramenta de diagnóstico de chamada](images/Dn451255.30501ba7-22d1-4db1-9297-56cf7dc6721c(OCS.15).png "Resultados do teste de utilização da ferramenta de diagnóstico de chamada")</span><span class="sxs-lookup"><span data-stu-id="ee3e7-146">![PreCall Diagnostic Tool Utilization test results](images/Dn451255.30501ba7-22d1-4db1-9297-56cf7dc6721c(OCS.15).png "PreCall Diagnostic Tool Utilization test results")</span></span>

</div>

<span id="running"></span>

<div>

## <a name="running-lync-pcd"></a><span data-ttu-id="ee3e7-147">Executando o Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ee3e7-147">Running Lync PCD</span></span>

<div>

## <a name="running-windows-desktop-app"></a><span data-ttu-id="ee3e7-148">Executando o aplicativo da área de trabalho do Windows</span><span class="sxs-lookup"><span data-stu-id="ee3e7-148">Running Windows Desktop App</span></span>

1.  <span data-ttu-id="ee3e7-149">Para iniciar o PCD em um sistema Windows 7, selecione o recurso de **diagnóstico de chamadas** no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="ee3e7-149">To start the PCD on a Windows 7 system, select **PreCall Diagnostics** from the **Start** menu.</span></span>
    
    <span data-ttu-id="ee3e7-150">Para iniciar o PCD em um sistema do Windows 8, selecione o ícone na tela inicial ou procure por "getcall Diagnostics".</span><span class="sxs-lookup"><span data-stu-id="ee3e7-150">To start the PCD on a Windows 8 system, select the icon on your Start screen, or search for “PreCall Diagnostics.”</span></span>
    
    <span data-ttu-id="ee3e7-151">![Ícone da ferramenta de diagnóstico de chamada](images/Dn451255.c9800fde-54f6-4efe-bb35-1a38064ec380(OCS.15).png "Ícone da ferramenta de diagnóstico de chamada")</span><span class="sxs-lookup"><span data-stu-id="ee3e7-151">![PreCall Diagnostic tool icon](images/Dn451255.c9800fde-54f6-4efe-bb35-1a38064ec380(OCS.15).png "PreCall Diagnostic tool icon")</span></span>

2.  <span data-ttu-id="ee3e7-152">Quando a ferramenta for iniciada, selecione seu método preferido de fornecimento de credenciais e selecione o modo operacional de rede na caixa de diálogo **Opções da ferramenta de diagnóstico de chamadas** e, em seguida, selecione **OK**:</span><span class="sxs-lookup"><span data-stu-id="ee3e7-152">When the tool starts, select your preferred method of providing credentials and select the network operating mode in the **PreCall Diagnostics Tool Options** dialog box, then select **OK**:</span></span>

3.  <span data-ttu-id="ee3e7-153">Selecione o botão **Iniciar teste** para começar a executar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-153">Select the **Start Test** button to start running diagnostics.</span></span>
    
    <span data-ttu-id="ee3e7-154">Se você tiver selecionado a opção **usar credenciais de rede** , o teste começará imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-154">If you selected the **Use network credentials** option, the test begins immediately.</span></span>
    
    <span data-ttu-id="ee3e7-155">Se você tiver selecionado a opção **deixe-me digitar minhas credenciais** , a caixa de diálogo **segurança do Windows** será aberta.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-155">If you selected the **Let me enter my credentials** option, the **Windows Security** dialog box opens.</span></span> <span data-ttu-id="ee3e7-156">Depois de inserir suas credenciais, o teste é iniciado.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-156">After you enter your credentials, the test starts.</span></span>

</div>

</div>

<span id="uninstall"></span>

<div>

## <a name="uninstalling-lync-pcd"></a><span data-ttu-id="ee3e7-157">Desinstalar o Lync PCD</span><span class="sxs-lookup"><span data-stu-id="ee3e7-157">Uninstalling Lync PCD</span></span>

<span data-ttu-id="ee3e7-158">Para remover o Lync PCD, siga o procedimento para seu sistema operacional:</span><span class="sxs-lookup"><span data-stu-id="ee3e7-158">To remove Lync PCD, follow the procedure for your operating system:</span></span>

  - <span data-ttu-id="ee3e7-159">Em um sistema Windows 7, abra o **painel de controle**, selecione **programas e recursos** e clique duas vezes em **diagnóstico de chamada do Lync 2013**.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-159">On a Windows 7 system, open the **Control Panel**, select **Programs and Features**, and double-click **Lync 2013 PreCall Diagnostics**.</span></span>

  - <span data-ttu-id="ee3e7-160">Em um sistema Windows 8, clique com o botão direito do mouse no bloco do PCD e clique em **desinstalar** na barra de aplicativos na parte inferior da tela iniciar.</span><span class="sxs-lookup"><span data-stu-id="ee3e7-160">On a Windows 8 system, right-click on the PCD tile and click **Uninstall** from the app bar at the bottom of the start screen.</span></span>

<span data-ttu-id="ee3e7-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee3e7-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

