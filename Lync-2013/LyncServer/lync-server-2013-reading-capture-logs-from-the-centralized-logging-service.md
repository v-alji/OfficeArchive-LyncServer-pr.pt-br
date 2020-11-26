---
title: 'Lync Server 2013: lendo logs de captura do serviço de log centralizado'
description: 'Lync Server 2013: lendo logs de captura do serviço de log centralizado.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reading capture logs from the Centralized Logging Service
ms:assetid: c86ccf61-d86f-4ebd-b8d1-984a1b73005d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721879(v=OCS.15)
ms:contentKeyID: 49733813
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fcdd70c924b49098814e80a375ae34d2bf48dc41
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436750"
---
# <a name="reading-capture-logs-from-the-centralized-logging-service-in-lync-server-2013"></a><span data-ttu-id="37900-103">Ler logs de captura do serviço de log centralizado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37900-103">Reading capture logs from the Centralized Logging Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37900-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37900-104">

<span> </span></span></span>

<span data-ttu-id="37900-105">_**Tópico da última modificação:** 2016-12-28_</span><span class="sxs-lookup"><span data-stu-id="37900-105">_**Topic Last Modified:** 2016-12-28_</span></span>

<span data-ttu-id="37900-106">Você percebe o verdadeiro benefício do serviço de registro centralizado depois de executar a pesquisa e tem um arquivo que pode ser usado para rastrear um problema relatado.</span><span class="sxs-lookup"><span data-stu-id="37900-106">You realize the real benefit of the Centralized Logging Service after you run the search and you have a file that you can use to track down a reported problem.</span></span> <span data-ttu-id="37900-107">Há várias maneiras de ler o arquivo.</span><span class="sxs-lookup"><span data-stu-id="37900-107">There are a number of ways that you can read the file.</span></span> <span data-ttu-id="37900-108">O arquivo de saída está em um formato de texto padrão e você pode usar Notepad.exe ou qualquer outro programa que permita a abertura e leitura de um arquivo de texto.</span><span class="sxs-lookup"><span data-stu-id="37900-108">The output file is in a standard text format and you can use Notepad.exe or any other programs that will allow you to open and read a text file.</span></span> <span data-ttu-id="37900-109">Para arquivos maiores e problemas mais complexos, você pode usar uma ferramenta como Snooper.exe projetada para ler e analisar a saída de log do serviço de log centralizado.</span><span class="sxs-lookup"><span data-stu-id="37900-109">For larger files and more complex issues, you could use a tool like Snooper.exe that is designed to read and parse the logging output from the Centralized Logging Service.</span></span> <span data-ttu-id="37900-110">O Snooper está incluído nas ferramentas de depuração do Lync Server 2013 disponíveis como um download separado.</span><span class="sxs-lookup"><span data-stu-id="37900-110">Snooper is included with the Lync Server 2013 Debug Tools that are available as a separate download.</span></span> <span data-ttu-id="37900-111">Você pode baixar as ferramentas de depuração do Lync Server 2013 aqui: [https://go.microsoft.com/fwlink/?LinkId=285257](https://go.microsoft.com/fwlink/?linkid=285257) .</span><span class="sxs-lookup"><span data-stu-id="37900-111">You can download the Lync Server 2013 Debug Tools here: [https://go.microsoft.com/fwlink/?LinkId=285257](https://go.microsoft.com/fwlink/?linkid=285257).</span></span> <span data-ttu-id="37900-112">Quando você instala as ferramentas de depuração do Lync Server 2013, pequenos atalhos e itens de menu não são criados.</span><span class="sxs-lookup"><span data-stu-id="37900-112">When you install the Lync Server 2013 Debug Tools, short cuts and menu items are not created.</span></span> <span data-ttu-id="37900-113">Depois de instalar as ferramentas de depuração do Lync Server 2013, abra o Windows Explorer, uma janela de linha de comando ou o Shell de gerenciamento do Lync Server e vá para o diretório (local padrão) C: \\ arquivos de programas \\ Microsoft Lync Server 2013 \\ ferramentas de depuração.</span><span class="sxs-lookup"><span data-stu-id="37900-113">After you install the Lync Server 2013 Debug Tools, open Windows Explorer, a command-line window, or Lync Server Management Shell and go to the directory (default location) C:\\Program Files\\Microsoft Lync Server 2013\\Debugging Tools.</span></span> <span data-ttu-id="37900-114">Clique duas vezes Snooper.exe ou digite Snooper.exe e, em seguida, pressione ENTER se estiver usando a linha de comando ou o Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="37900-114">Double-click Snooper.exe or type Snooper.exe, and then press ENTER if you are using the command line or Lync Server Management Shell.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="37900-115">A intenção deste tópico não é detalhar e discutir técnicas de resolução de problemas.</span><span class="sxs-lookup"><span data-stu-id="37900-115">The intent of this topic is not to detail and discuss troubleshooting techniques.</span></span> <span data-ttu-id="37900-116">A resolução de problemas e os processos relacionados é um assunto complexo.</span><span class="sxs-lookup"><span data-stu-id="37900-116">Troubleshooting and the processes around it is a complex subject.</span></span> <span data-ttu-id="37900-117">Para obter detalhes sobre como solucionar problemas de noções básicas e solucionar problemas de cargas de trabalho específicas, consulte o Microsoft Lync Server 2010 Resource Kit Book <A href="https://go.microsoft.com/fwlink/p/?linkid=211003">https://go.microsoft.com/fwlink/p/?linkId=211003</A> .</span><span class="sxs-lookup"><span data-stu-id="37900-117">For details about troubleshooting basics and troubleshooting specific workloads, see the Microsoft Lync Server 2010 Resource Kit book at <A href="https://go.microsoft.com/fwlink/p/?linkid=211003">https://go.microsoft.com/fwlink/p/?linkId=211003</A>.</span></span> <span data-ttu-id="37900-118">Os processos e procedimentos ainda se aplicam ao Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37900-118">The processes and procedures still apply to Lync Server 2013.</span></span>



</div>

<span data-ttu-id="37900-119">O Lync Server 2013 apresenta uma versão atualizada do Espionador que inclui alguns recursos novos.</span><span class="sxs-lookup"><span data-stu-id="37900-119">Lync Server 2013 introduces an updated version of Snooper that includes some new features.</span></span> <span data-ttu-id="37900-120">A captura de tela a seguir mostra a versão do Espionador do Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="37900-120">The following screen shot shows the version of Snooper from Office Communications Server 2007.</span></span>

<span data-ttu-id="37900-121">![Versão do Office Communications 2007 do Espionador.](images/JJ721879.129503a8-8edd-4bb0-a68f-c43f9a548b93(OCS.15).jpg "Versão do Office Communications 2007 do Espionador.")</span><span class="sxs-lookup"><span data-stu-id="37900-121">![Office Communications 2007 version of Snooper.](images/JJ721879.129503a8-8edd-4bb0-a68f-c43f9a548b93(OCS.15).jpg "Office Communications 2007 version of Snooper.")</span></span>

<span data-ttu-id="37900-122">A captura de tela a seguir mostra a nova versão do Espionador incluída nas ferramentas de depuração do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37900-122">The following screen shot shows the new version of Snooper included in the Lync Server 2013 Debug Tools.</span></span>

<span data-ttu-id="37900-123">![Versão do Espionador do Lync Server 2013.](images/JJ721879.131495dd-8220-4ae4-af37-0ac5c318fd45(OCS.15).jpg "Versão do Espionador do Lync Server 2013.")</span><span class="sxs-lookup"><span data-stu-id="37900-123">![Lync Server 2013 version of Snooper.](images/JJ721879.131495dd-8220-4ae4-af37-0ac5c318fd45(OCS.15).jpg "Lync Server 2013 version of Snooper.")</span></span>

<span data-ttu-id="37900-124">A captura de tela a seguir mostra a barra de ferramentas com funções usadas com frequência.</span><span class="sxs-lookup"><span data-stu-id="37900-124">The following screen shot shows the toolbar with frequently used functions.</span></span>

<span data-ttu-id="37900-125">![Barra de ferramentas do espionador 2013.](images/JJ721879.989249c5-a33e-4251-b8b4-411019cc12b2(OCS.15).jpg "Barra de ferramentas do espionador 2013.")</span><span class="sxs-lookup"><span data-stu-id="37900-125">![Snooper 2013 toolbar.](images/JJ721879.989249c5-a33e-4251-b8b4-411019cc12b2(OCS.15).jpg "Snooper 2013 toolbar.")</span></span>

<span data-ttu-id="37900-126">Além disso, o recurso mais recente que adiciona valor é o modo de exibição de diagrama de fluxograma (fluxo de chamadas).</span><span class="sxs-lookup"><span data-stu-id="37900-126">And, the newest feature that adds value is the Flow Chart (call flow) diagram view.</span></span> <span data-ttu-id="37900-127">Selecione um fluxo de mensagens na guia **mensagem** e clique no botão **fluxo de chamadas** .</span><span class="sxs-lookup"><span data-stu-id="37900-127">You select a message flow in the **Message** tab and click the **Call Flow** button.</span></span> <span data-ttu-id="37900-128">Ao passar pelas mensagens, o diagrama de fluxo de chamadas é atualizado com novos dados.</span><span class="sxs-lookup"><span data-stu-id="37900-128">As you proceed through the messages, the call flow diagram updates with new data.</span></span>

<span data-ttu-id="37900-129">![Diagrama de fluxo de chamadas do espionador 2013.](images/JJ721879.bb8be45d-a842-48fe-86f8-380207d70bab(OCS.15).jpg "Diagrama de fluxo de chamadas do espionador 2013.")</span><span class="sxs-lookup"><span data-stu-id="37900-129">![Snooper 2013 call flow diagram.](images/JJ721879.bb8be45d-a842-48fe-86f8-380207d70bab(OCS.15).jpg "Snooper 2013 call flow diagram.")</span></span>

<span data-ttu-id="37900-130">Você pode passar o mouse sobre o modo de exibição de diagrama e obter detalhes sobre as mensagens e o conteúdo dos fluxos e mensagens, bem como os elementos do servidor.</span><span class="sxs-lookup"><span data-stu-id="37900-130">You can hover over the diagram view and get details about the messages and content of the flows and messages as well as the server elements.</span></span> <span data-ttu-id="37900-131">Clique em qualquer seta de fluxo de chamadas para ir até a mensagem no modo de exibição mensagens.</span><span class="sxs-lookup"><span data-stu-id="37900-131">Click on any call flow arrow to go to the message in the Messages view.</span></span>

<span data-ttu-id="37900-132">![Detalhes da mensagem do diagrama de fluxo de chamadas.](images/JJ721879.1147d720-38a9-4bda-8361-78f27ecde3d1(OCS.15).jpg "Detalhes da mensagem do diagrama de fluxo de chamadas.")</span><span class="sxs-lookup"><span data-stu-id="37900-132">![Call flow diagram message details.](images/JJ721879.1147d720-38a9-4bda-8361-78f27ecde3d1(OCS.15).jpg "Call flow diagram message details.")</span></span>

<div>

## <a name="to-open-a-log-file-in-snooper"></a><span data-ttu-id="37900-133">Para abrir um arquivo de log no Snooper</span><span class="sxs-lookup"><span data-stu-id="37900-133">To open a log file in Snooper</span></span>

1.  <span data-ttu-id="37900-p106">Para usar o Snooper e abrir arquivos de log, você precisará de acesso de leitura aos arquivos de log. Para usar o Snooper e acessar os arquivos de log, você deve ser membro dos grupos de segurança RBAC CsAdministrator ou CsServerAdministrator ou uma função RBAC personalizada que contém um desses dois grupos.</span><span class="sxs-lookup"><span data-stu-id="37900-p106">To use Snooper and open log files, you need read access to the log files. To use Snooper and access the log files you must be a member of the CsAdministrator or the CsServerAdministrator role-based access control (RBAC) security groups, or a custom RBAC role that contains either of these two groups.</span></span>

2.  <span data-ttu-id="37900-136">Após a instalação das ferramentas de depuração do Lync Server (LyncDebugTools.msi), altere diretório para o local do Snooper.exe usando o Windows Explorer ou a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="37900-136">After the installation of the Lync Server Debugging Tools (LyncDebugTools.msi), change directory to the location of Snooper.exe using Windows Explorer or from the command line.</span></span> <span data-ttu-id="37900-137">Por padrão, as ferramentas de depuração estão localizadas em C: \\ arquivos de programa \\ ferramentas de depuração do Microsoft Lync Server 2013 \\ .</span><span class="sxs-lookup"><span data-stu-id="37900-137">By default, the debugging tools are located in C:\\Program Files\\Microsoft Lync Server 2013\\Debugging Tools.</span></span> <span data-ttu-id="37900-138">Clique duas vezes ou execute Snooper.exe.</span><span class="sxs-lookup"><span data-stu-id="37900-138">Double-click or run Snooper.exe.</span></span>

3.  <span data-ttu-id="37900-139">Após o Snooper estar aberto, clique com o botão direito em **Arquivo**, clique em **Abrir arquivo**, encontre seus arquivos de registro, selecione um arquivo na caixa de diálogo **Abrir** e clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="37900-139">After Snooper is open, right-click **File**, click **OpenFile**, find your log files, select a file in the **Open** dialog box, and then click **Open**.</span></span>

4.  <span data-ttu-id="37900-140">As mensagens de **Rastreamento** do arquivo de log são exibidas na guia **Rastreamento**. Clique na guia **Mensagens** para exibir o conteúdo da mensagem dos rastreamentos coletados.</span><span class="sxs-lookup"><span data-stu-id="37900-140">The log file’s **Trace** messages are displayed on the **Trace** tab. Click the **Messages** tab to view the message contents of the collected traces.</span></span>

</div>

<div>

## <a name="to-display-a-call-flow-diagram"></a><span data-ttu-id="37900-141">Para exibir um fluxograma da chamada</span><span class="sxs-lookup"><span data-stu-id="37900-141">To display a call flow diagram</span></span>

1.  <span data-ttu-id="37900-p108">Para usar o Snooper e abrir arquivos de log, você precisa de acesso de leitura dos arquivos de log. Para usar o Snooper e acessar os arquivos de log, você precisará ser um membro dos grupos de segurança RBAC CsAdministrator ou CsServerAdministrator ou uma função RBAC personalizada que contém um destes dois grupos.</span><span class="sxs-lookup"><span data-stu-id="37900-p108">To use Snooper and open log files, you need read access to the log files. To use Snooper and access the log files, you need to be a member of the CsAdministrator or the CsServerAdministrator role-based access control (RBAC) security groups, or a custom RBAC role that contains either of these two groups.</span></span>

2.  <span data-ttu-id="37900-144">Abra um arquivo de log e clique na guia **Mensagens**, selecione uma conversa na exibição de mensagens ou selecione um componente de rastreamento na guia **Rastreamento**.</span><span class="sxs-lookup"><span data-stu-id="37900-144">Open a log file and click the **Messages** tab, select a conversation in the messages view or select a trace component on the **Trace** tab.</span></span>

3.  <span data-ttu-id="37900-145">Clique em **Fluxo de chamadas**.</span><span class="sxs-lookup"><span data-stu-id="37900-145">Click **Call Flow**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="37900-p109">Se você clicar em uma mensagem ou rastreamento que não faz parte do fluxo de chamadas, o diagrama não aparecerá e uma mensagem de status aparece na parte inferior do Snooper dizendo “Esta mensagem não é elegível para fluxo de chamadas”. Escolha outra mensagem ou rastreamento e o fluxo de chamadas aparecerá se a mensagem ou o rastreamento faz parte de um fluxo de chamadas.</span><span class="sxs-lookup"><span data-stu-id="37900-p109">If you click on a message or trace that is not part of a call flow, the diagram will not appear and a status message appears at the bottom of Snooper stating “This message is not eligible for callfow”. Choose another message or trace and the call flow will appear if the message or trace is part of a call flow.</span></span>

    
    </div>

4.  <span data-ttu-id="37900-148">Mova pelas Mensagens ou linhas de Rastreamento e observe se o fluxograma de chamada atualiza ou muda para exibir um novo diagrama.</span><span class="sxs-lookup"><span data-stu-id="37900-148">Move through the Messages or the Trace lines and note whether the call flow diagram updates or changes to display a new diagram.</span></span>

5.  <span data-ttu-id="37900-149">Passe sobre os elementos para obter informações sobre mensagens de chamada, pontos de extremidade e outros componentes.</span><span class="sxs-lookup"><span data-stu-id="37900-149">Hover over elements to get information about call messages, endpoints, and other components.</span></span>

<span data-ttu-id="37900-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37900-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

