---
title: 'Lync Server 2013: Importar um arquivo de configuração de rota de voz'
description: 'Lync Server 2013: importar um arquivo de configuração de rota de voz.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Import a voice route configuration file
ms:assetid: 4bac05e5-ed8b-4f10-96b0-b8a65ff356ec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398301(v=OCS.15)
ms:contentKeyID: 48184049
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 994095598b39548f00447edd4b0d322a7ec5545e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427331"
---
# <a name="import-a-voice-route-configuration-file-in-lync-server-2013"></a><span data-ttu-id="d1563-103">Importar um arquivo de configuração de rota de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1563-103">Import a voice route configuration file in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d1563-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d1563-104">

<span> </span></span></span>

<span data-ttu-id="d1563-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="d1563-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="d1563-106">Se você quiser salvar sua configuração de roteamento de voz sem publicá-la, siga estas etapas para usar os comandos de exportação e importação de configuração do painel de controle do Lync Server para salvar e recuperar um instantâneo de sua configuração de roteamento de voz.</span><span class="sxs-lookup"><span data-stu-id="d1563-106">If you want to save your voice routing configuration without publishing it, follow these steps to use the Lync Server Control Panel configuration export and import commands to save and retrieve a snapshot of your voice routing configuration.</span></span> <span data-ttu-id="d1563-107">Quando você importa um arquivo de configuração de roteamento de voz (. vcfg), mas foram feitas alterações na configuração de roteamento de voz no servidor enquanto isso, as páginas no grupo de **Roteamento de voz** no painel de controle do Lync Server indicam que há alterações não confirmadas no roteamento de voz.</span><span class="sxs-lookup"><span data-stu-id="d1563-107">When you import a voice routing configuration file (.vcfg), but changes have been made to the voice routing configuration on the server in the meantime, the pages in the **Voice Routing** group in Lync Server Control Panel will indicate that there are uncommitted changes to voice routing.</span></span> <span data-ttu-id="d1563-108">Essas alterações não confirmadas são as diferenças entre as duas configurações que exigem reconciliação.</span><span class="sxs-lookup"><span data-stu-id="d1563-108">Those uncommitted changes are the differences between the two configurations that require reconciliation.</span></span>

<span data-ttu-id="d1563-109">Se você tiver feito alterações não confirmadas nas configurações de qualquer página do grupo, as alterações serão salvas no arquivo de configuração de voz exportado (. vcfg).</span><span class="sxs-lookup"><span data-stu-id="d1563-109">If you have made any uncommitted changes to the settings on any page within the group, the changes are saved in the exported voice configuration file (.vcfg).</span></span> <span data-ttu-id="d1563-110">Isso permite que você faça alterações de configuração de roteamento de voz durante várias sessões antes de publicar as alterações.</span><span class="sxs-lookup"><span data-stu-id="d1563-110">This enables you to make voice routing configuration changes during multiple sessions before you publish the changes.</span></span>

<div>

## <a name="to-import-a-voice-routing-configuration"></a><span data-ttu-id="d1563-111">Para importar uma configuração de roteamento de voz</span><span class="sxs-lookup"><span data-stu-id="d1563-111">To import a voice routing configuration</span></span>

1.  <span data-ttu-id="d1563-112">Faça logon no computador como um membro do grupo RTCUniversalServerAdmins ou como um membro da função CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="d1563-112">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="d1563-113">Para obter detalhes, consulte [delegar permissões de configuração no Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="d1563-113">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="d1563-114">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="d1563-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d1563-115">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d1563-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d1563-116">Na barra de navegação esquerda, clique em **Roteamento de Voz**.</span><span class="sxs-lookup"><span data-stu-id="d1563-116">In the left navigation bar, click **Voice Routing**.</span></span>

4.  <span data-ttu-id="d1563-117">No menu **Ações**, clique em **Importar Configuração**.</span><span class="sxs-lookup"><span data-stu-id="d1563-117">On the **Actions** menu, click **Import configuration**.</span></span>

5.  <span data-ttu-id="d1563-118">Localize o arquivo de configuração que você deseja importar e clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="d1563-118">Find the configuration file you want to import and then click **Open**.</span></span>

6.  <span data-ttu-id="d1563-119">Clique em **Confirmar** e, em seguida, clique em **Confirmar tudo**.</span><span class="sxs-lookup"><span data-stu-id="d1563-119">Click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d1563-120">Sempre que importar um arquivo de configuração de voz, você deve executar o comando <STRONG>Confirmar tudo</STRONG> para publicar a alteração na configuração.</span><span class="sxs-lookup"><span data-stu-id="d1563-120">Whenever you import a voice configuration file, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="d1563-121">Para obter detalhes, consulte <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">publicar alterações pendentes na configuração de roteamento de voz no Lync Server 2013</A> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="d1563-121">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d1563-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1563-122">See Also</span></span>


[<span data-ttu-id="d1563-123">Exportar um arquivo de configuração de rota de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1563-123">Export a voice route configuration file in Lync Server 2013</span></span>](lync-server-2013-export-a-voice-route-configuration-file.md)  
[<span data-ttu-id="d1563-124">Publicar alterações pendentes na configuração de roteamento de voz no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1563-124">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  
  

<span data-ttu-id="d1563-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d1563-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

