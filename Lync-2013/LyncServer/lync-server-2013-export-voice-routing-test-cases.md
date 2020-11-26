---
title: 'Lync Server 2013: Exportar casos de teste de roteamento de voz'
description: 'Lync Server 2013: exportar casos de teste de roteamento de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Export voice routing test cases
ms:assetid: 489ac472-1a35-4755-b390-48f7cdf31e94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425957(v=OCS.15)
ms:contentKeyID: 48184050
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 934bd183a17c46cf82fe5bc04faaa55a9bbe4731
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428346"
---
# <a name="export-voice-routing-test-cases-in-lync-server-2013"></a><span data-ttu-id="033f2-103">Exportar casos de teste de roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="033f2-103">Export voice routing test cases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="033f2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="033f2-104">

<span> </span></span></span>

<span data-ttu-id="033f2-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="033f2-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="033f2-106">Os casos de teste fornecem uma maneira de testar as rotas de voz em sua organização: você define itens como o número a ser discado e o plano de discagem e a política de voz a ser empregado, e o Lync Server pode, em seguida, verificar se, dadas essas condições, o número fornecido pode ser roteado com êxito para a rede PSTN.</span><span class="sxs-lookup"><span data-stu-id="033f2-106">Test cases provide a way for you to test voice routes in your organization: you define such things as the number to be dialed and the dial plan and voice policy to be employed, and Lync Server can then verify that, given those conditions, the supplied number can successfully be routed to the PSTN network.</span></span>

<span data-ttu-id="033f2-107">Os casos de teste, que podem ser criados usando o painel de controle do Lync Server, geralmente são salvos apenas no servidor em que o caso foi originalmente criado e executado.</span><span class="sxs-lookup"><span data-stu-id="033f2-107">Test cases, which can be created by using Lync Server Control Panel, are typically saved only on the server where the case was originally created and run.</span></span> <span data-ttu-id="033f2-108">No entanto, esses casos de teste podem ser exportados como arquivos XML (com a extensão. vtest) e depois importados em outros servidores.</span><span class="sxs-lookup"><span data-stu-id="033f2-108">However, these test cases can be exported as XML files (with the .vtest extension) and then imported on other servers.</span></span> <span data-ttu-id="033f2-109">Isso permite que você execute os mesmos testes em computadores diferentes localizados em diferentes pontos da topologia.</span><span class="sxs-lookup"><span data-stu-id="033f2-109">This enables you to run the same tests on different computers located at different points in your topology.</span></span>

<div>

## <a name="to-export-a-voice-routing-test-case"></a><span data-ttu-id="033f2-110">Para exportar um caso de teste de roteamento de voz</span><span class="sxs-lookup"><span data-stu-id="033f2-110">To export a voice routing test case</span></span>

1.  <span data-ttu-id="033f2-111">No painel de controle do Lync Server, clique em **Roteamento de voz** e, em seguida, clique em **testar roteamento de voz**.</span><span class="sxs-lookup"><span data-stu-id="033f2-111">In Lync Server Control Panel, click **Voice Routing** and then click **Test Voice Routing**.</span></span>

2.  <span data-ttu-id="033f2-112">Na guia **Roteamento de voz de teste** , selecione o caso de teste (ou casos de teste) a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="033f2-112">On the **Test Voice Routing** tab, select the test case (or test cases) to be exported.</span></span> <span data-ttu-id="033f2-113">Para selecionar vários casos de teste, clique no primeiro caso para ser exportado, mantenha a tecla Ctrl pressionada e selecione os casos adicionais a serem exportados.</span><span class="sxs-lookup"><span data-stu-id="033f2-113">To select multiple test cases, click the first case to be exported, then hold down the Ctrl key and select the additional cases to be exported.</span></span>

3.  <span data-ttu-id="033f2-114">Clique em **ação** e, em seguida, clique em **Exportar casos de teste**.</span><span class="sxs-lookup"><span data-stu-id="033f2-114">Click **Action**, then click **Export test cases**.</span></span>

4.  <span data-ttu-id="033f2-115">Na caixa de diálogo **salvar como** , selecione uma pasta para armazenar os casos de teste exportados e digite um nome para o arquivo XML resultante na caixa **nome do arquivo** .</span><span class="sxs-lookup"><span data-stu-id="033f2-115">In the **Save As** dialog box, select a folder to store the exported test cases and type a name for the resulting XML file in the **File name** box.</span></span> <span data-ttu-id="033f2-116">Observe que, se você estiver exportando vários casos vários testes, todos esses casos de teste serão salvos em um único arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="033f2-116">Note that if you are exporting multiple tests cases all of these test cases will be saved to a single XML file.</span></span>

5.  <span data-ttu-id="033f2-117">Para salvar os casos de teste, clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="033f2-117">To save the test cases, click **Save**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="033f2-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="033f2-118">See Also</span></span>


[<span data-ttu-id="033f2-119">Importar casos de teste de roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="033f2-119">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)  
  

<span data-ttu-id="033f2-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="033f2-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

