---
title: 'Lync Server 2013: solução de problemas com o plug-in VDI do Lync'
description: 'Lync Server 2013: solução de problemas do plug-in VDI do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Troubleshooting the Lync VDI plug-in
ms:assetid: 183c9449-b907-409c-b5ed-b02af3bd93ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204713(v=OCS.15)
ms:contentKeyID: 48183525
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3cd2c0e3c8a47225f00ce280706dea2287e4dc8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389950"
---
# <a name="troubleshooting-the-lync-vdi-plug-in-in-lync-server-2013"></a><span data-ttu-id="ea0d2-103">Solução de problemas do plug-in VDI do Lync no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ea0d2-103">Troubleshooting the Lync VDI plug-in in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ea0d2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ea0d2-104">

<span> </span></span></span>

<span data-ttu-id="ea0d2-105">_**Tópico da última modificação:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="ea0d2-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<div>

## <a name="troubleshooting-issues-with-installing-the-lync-vdi-plug-in-on-a-thin-client"></a><span data-ttu-id="ea0d2-106">Solucionando problemas com a instalação do plug-in VDI do Lync em um cliente Thin</span><span class="sxs-lookup"><span data-stu-id="ea0d2-106">Troubleshooting Issues with Installing the Lync VDI Plug-in on a Thin Client</span></span>

<span data-ttu-id="ea0d2-107">Se houver problemas para instalar o plug-in VDI em um cliente leve, verifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ea0d2-107">If there are issues with installing the VDI plug-in on a thin client, check the following:</span></span>

  - <span data-ttu-id="ea0d2-108">Verifique se há espaço em disco suficiente na pasta que você especificou nas variáveis do sistema TEMP e TMP.</span><span class="sxs-lookup"><span data-stu-id="ea0d2-108">Ensure that there is sufficient space in the folder that you specified in the TEMP and TMP system variables.</span></span>

  - <span data-ttu-id="ea0d2-p101">Verifique se a proteção contra gravação está desativada. Consulte a documentação do fabricante do seu dispositivo para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="ea0d2-p101">Ensure that write-protect is turned off. Refer to your device manufacturer’s documentation for instructions.</span></span>

</div>

<div>

## <a name="troubleshooting-issues-with-pairing"></a><span data-ttu-id="ea0d2-111">Solução de problemas de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="ea0d2-111">Troubleshooting Issues with Pairing</span></span>

<span data-ttu-id="ea0d2-112">Quando o emparelhamento de plug-in do VDI falha, o ícone de emparelhamento no canto inferior direito é exibido como um "X" vermelho, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="ea0d2-112">When VDI plug-in pairing fails, the pairing icon in the lower right displays as a red “X” as shown:</span></span>

<span data-ttu-id="ea0d2-113">![Ícone de VDI do Lync mostrando o emparelhamento com êxito](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Ícone de VDI do Lync mostrando o emparelhamento com êxito")</span><span class="sxs-lookup"><span data-stu-id="ea0d2-113">![Lync VDI icon showing successful pairing](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Lync VDI icon showing successful pairing")</span></span>

<span data-ttu-id="ea0d2-114">Estes são os possíveis motivos para falhas e as ações corretivas que você pode executar.</span><span class="sxs-lookup"><span data-stu-id="ea0d2-114">The following are possible reasons for failures and the corrective actions you can take.</span></span>

  - <span data-ttu-id="ea0d2-115">**O usuário inseriu credenciais incorretas durante a entrada.**</span><span class="sxs-lookup"><span data-stu-id="ea0d2-115">**The user entered incorrect credentials during sign-in.**</span></span>
    
    <span data-ttu-id="ea0d2-116">O usuário deve desconectar-se do Lync e entrar novamente com as credenciais corretas.</span><span class="sxs-lookup"><span data-stu-id="ea0d2-116">The user should sign out of Lync and sign in again with the correct credentials.</span></span> <span data-ttu-id="ea0d2-117">A caixa de diálogo de emparelhamento será exibida novamente e mostrará se o emparelhamento foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ea0d2-117">The pairing dialog box will reappear and show whether pairing is successful.</span></span>

  - <span data-ttu-id="ea0d2-118">**Outra instância do cliente de área de trabalho remota está sendo executada.**</span><span class="sxs-lookup"><span data-stu-id="ea0d2-118">**Another instance of the remote desktop client is running.**</span></span>
    
    <span data-ttu-id="ea0d2-119">Se eles estiverem usando a conexão de área de trabalho remota no Windows, os usuários devem fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ea0d2-119">If they are using Remote Desktop Connection in Windows, users should do the following:</span></span>
    
    1.  <span data-ttu-id="ea0d2-120">Iniciar o Gerenciador de Tarefas: pressionar **Alt+Ctrl+Delete** e depois clicar em **Iniciar Gerenciador de Tarefas**.</span><span class="sxs-lookup"><span data-stu-id="ea0d2-120">Start Task Manager: Press **Alt+Ctrl+Delete**, and then click **Start Task Manager**.</span></span>
    
    2.  <span data-ttu-id="ea0d2-121">Clicar na guia **Processos** e procurar todos os processos chamados **mstsc.exe** na lista.</span><span class="sxs-lookup"><span data-stu-id="ea0d2-121">Click the **Processes** tab and look for all processes named **mstsc.exe** in the list.</span></span>
    
    3.  <span data-ttu-id="ea0d2-122">Realçar cada processo **mstsc.exe** e clicar em **Finalizar Processo**. </span><span class="sxs-lookup"><span data-stu-id="ea0d2-122">Highlight each **mstsc.exe** process and then click **End Process**.</span></span>
    
    4.  <span data-ttu-id="ea0d2-123">Iniciar uma nova sessão de área de trabalho remota e tentar conectar-se novamente. </span><span class="sxs-lookup"><span data-stu-id="ea0d2-123">Start a new remote desktop session and try connecting again.</span></span>

  - <span data-ttu-id="ea0d2-124">**Os arquivos necessários não foram instalados corretamente.**</span><span class="sxs-lookup"><span data-stu-id="ea0d2-124">**The necessary files did not install correctly.**</span></span>
    
    <span data-ttu-id="ea0d2-125">Após a instalação do plug-in no computador local, os seguintes arquivos devem estar presentes em C: \\ arquivos de programas \\ Microsoft Office \\ Office15 (ou na letra de unidade apropriada):</span><span class="sxs-lookup"><span data-stu-id="ea0d2-125">After the plug-in is installed on the local computer, the following files should be present under C:\\Program Files\\Microsoft Office\\Office15 (or the appropriate drive letter):</span></span>
    
      - <span data-ttu-id="ea0d2-126">LyncVdiPlugin.dll</span><span class="sxs-lookup"><span data-stu-id="ea0d2-126">LyncVdiPlugin.dll</span></span>
    
      - <span data-ttu-id="ea0d2-127">UcVdi.dll</span><span class="sxs-lookup"><span data-stu-id="ea0d2-127">UcVdi.dll</span></span>
    
    <span data-ttu-id="ea0d2-128">Se houver algum problema com o emparelhamento com VDI, verifique se esses arquivos estão presentes no computador local.</span><span class="sxs-lookup"><span data-stu-id="ea0d2-128">If there are any issues with VDI pairing, check to make sure that these files are present on the local computer.</span></span>

  - <span data-ttu-id="ea0d2-129">**O cliente do Lync está em execução no computador local.**</span><span class="sxs-lookup"><span data-stu-id="ea0d2-129">**The Lync client is running on the local computer.**</span></span>
    
    <span data-ttu-id="ea0d2-130">Para usar o plug-in VDI do Lync, um cliente do Lync não deve estar em execução no computador local, caso contrário, haverá falha na junção.</span><span class="sxs-lookup"><span data-stu-id="ea0d2-130">To use the Lync VDI plugin, a Lync client must not be running on the local computer, otherwise pairing will fail.</span></span> <span data-ttu-id="ea0d2-131">Como prática recomendada, o usuário não deve instalar um cliente do Lync no computador local.</span><span class="sxs-lookup"><span data-stu-id="ea0d2-131">As a best practice, the user should not install a Lync client on the local computer.</span></span>

<span data-ttu-id="ea0d2-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ea0d2-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

