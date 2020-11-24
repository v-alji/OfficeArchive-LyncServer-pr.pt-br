---
title: 'Lync Server 2013: Importar casos de teste de roteamento de voz'
description: 'Lync Server 2013: importar casos de teste de roteamento de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Import voice routing test cases
ms:assetid: 6546e24c-9ad2-428b-92b2-63948ed0f884
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398460(v=OCS.15)
ms:contentKeyID: 48184325
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06ce1b144de03406b7b78d6957371ed2bc303e95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390241"
---
# <a name="import-voice-routing-test-cases-in-lync-server-2013"></a><span data-ttu-id="ddb0e-103">Importar casos de teste de roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddb0e-103">Import voice routing test cases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ddb0e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ddb0e-104">

<span> </span></span></span>

<span data-ttu-id="ddb0e-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ddb0e-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ddb0e-106">Os casos de teste fornecem uma maneira de testar as rotas de voz em sua organização: você define itens como o número a ser discado e o plano de discagem e a política de voz a ser empregado, e o Lync Server 2013 pode, em seguida, verificar se, dadas essas condições, o número fornecido pode ser roteado com êxito para a rede PSTN.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-106">Test cases provide a way for you to test voice routes in your organization: you define such things as the number to be dialed and the dial plan and voice policy to be employed, and Lync Server 2013 can then verify that, given those conditions, the supplied number can successfully be routed to the PSTN network.</span></span>

<span data-ttu-id="ddb0e-107">Os casos de teste, que podem ser criados usando o painel de controle do Lync Server, geralmente são salvos apenas no servidor em que o caso foi originalmente criado e executado.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-107">Test cases, which can be created by using Lync Server Control Panel, are typically saved only on the server where the case was originally created and run.</span></span> <span data-ttu-id="ddb0e-108">No entanto, esses casos de teste podem ser exportados como arquivos XML (com a extensão. vtest) e depois importados em outros servidores.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-108">However, these test cases can be exported as XML files (with the .vtest extension) and then imported on other servers.</span></span> <span data-ttu-id="ddb0e-109">Isso permite que você execute os mesmos testes em computadores diferentes localizados em diferentes pontos da topologia.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-109">This enables you to run the same tests on different computers located at different points in your topology.</span></span>

<div>

## <a name="to-import-a-voice-routing-test-case"></a><span data-ttu-id="ddb0e-110">Para importar um caso de teste de roteamento de voz</span><span class="sxs-lookup"><span data-stu-id="ddb0e-110">To import a voice routing test case</span></span>

1.  <span data-ttu-id="ddb0e-111">Faça logon no computador como um membro do grupo RTCUniversalServerAdmins ou como um membro da função CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-111">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="ddb0e-112">Para obter detalhes, consulte [delegar permissões de configuração no Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="ddb0e-112">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="ddb0e-113">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ddb0e-114">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ddb0e-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ddb0e-115">Na barra de navegação esquerdo, clique em **Roteamento de voz**.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-115">In the left navigation bar, click **Voice Routing**.</span></span>

4.  <span data-ttu-id="ddb0e-116">No menu **ações** , clique em **importar casos de teste**.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-116">On the **Actions** menu, click **Import test cases**.</span></span>

5.  <span data-ttu-id="ddb0e-117">Localize o arquivo de caso de teste (. vtest) que você deseja importar e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-117">Find the test case file (.vtest) that you want to import, and then click **Open**.</span></span>

6.  <span data-ttu-id="ddb0e-118">Clique em **Confirmar** e, em seguida, clique em **Confirmar tudo**.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-118">Click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ddb0e-119">Sempre que importar um arquivo. vtest, você deve executar o comando <STRONG>Commit All</STRONG> para publicar o caso de teste.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-119">Whenever you import a .vtest file, you must run the <STRONG>Commit all</STRONG> command to publish the test case.</span></span> <span data-ttu-id="ddb0e-120">Para obter detalhes, consulte <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">publicar alterações pendentes na configuração de roteamento de voz no Lync Server 2013</A> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="ddb0e-120">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ddb0e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddb0e-121">See Also</span></span>


[<span data-ttu-id="ddb0e-122">Exportar casos de teste de roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddb0e-122">Export voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-export-voice-routing-test-cases.md)  
  

<span data-ttu-id="ddb0e-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ddb0e-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

