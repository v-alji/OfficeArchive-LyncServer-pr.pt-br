---
title: 'Lync Server 2013: habilitar o estacionamento de chamadas para usuários'
description: 'Lync Server 2013: habilitar o estacionamento de chamadas para usuários.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Call Park for users
ms:assetid: 9430763f-3394-467c-9c6d-426bf761604e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398753(v=OCS.15)
ms:contentKeyID: 48184814
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c7f9ab23b9fa71943efafd588b8c57a2af781b08
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428934"
---
# <a name="enable-call-park-for-users-in-lync-server-2013"></a><span data-ttu-id="b898e-103">Habilitar o estacionamento de chamadas para usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b898e-103">Enable Call Park for users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b898e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b898e-104">

<span> </span></span></span>

<span data-ttu-id="b898e-105">_**Tópico da última modificação:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="b898e-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="b898e-106">Os usuários não podem estacionar chamadas nem recuperar chamadas estacionadas até que elas sejam habilitadas para estacionamento de chamadas na política de voz.</span><span class="sxs-lookup"><span data-stu-id="b898e-106">Users cannot park calls or retrieve parked calls until they are enabled for Call Park in voice policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b898e-107">Por padrão, o estacionamento de chamadas está desabilitado para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="b898e-107">By default, Call Park is disabled for all users.</span></span>



</div>

<span data-ttu-id="b898e-108">Você pode habilitar o estacionamento de chamadas no escopo global ou no escopo do site ou no escopo do usuário.</span><span class="sxs-lookup"><span data-stu-id="b898e-108">You can enable Call Park at the global scope, or at the site scope or user scope.</span></span> <span data-ttu-id="b898e-109">O escopo do usuário tem precedência sobre o escopo do site e o escopo do site tem precedência sobre o escopo global.</span><span class="sxs-lookup"><span data-stu-id="b898e-109">User scope takes precedence over site scope, and site scope takes precedence over global scope.</span></span> <span data-ttu-id="b898e-110">Se você tiver várias políticas de voz, examine todas as políticas para habilitar o estacionamento de chamadas, não apenas a política global.</span><span class="sxs-lookup"><span data-stu-id="b898e-110">If you have multiple voice policies, review all the policies to enable Call Park, not just the global policy.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-enable-call-park-for-users"></a><span data-ttu-id="b898e-111">Para usar o painel de controle do Lync Server para habilitar o estacionamento de chamadas para usuários</span><span class="sxs-lookup"><span data-stu-id="b898e-111">To Use Lync Server Control Panel to Enable Call Park for Users</span></span>

1.  <span data-ttu-id="b898e-112">Faça logon no computador como membro do grupo **RTCUniversalServerAdmins** ou como membro da função administrativa **CsVoiceAdministrator**, **CsServerAdministrator**, ou **CsAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="b898e-112">Log on to the computer as a member of the **RTCUniversalServerAdmins** group, or as a member of the **CsVoiceAdministrator**, **CsServerAdministrator**, or **CsAdministrator** administrative role.</span></span>

2.  <span data-ttu-id="b898e-113">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b898e-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="b898e-114">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b898e-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="b898e-115">Na barra de navegação esquerdo, clique em **Roteamento de voz**.</span><span class="sxs-lookup"><span data-stu-id="b898e-115">In the left navigation bar, click **Voice Routing**.</span></span>

4.  <span data-ttu-id="b898e-116">Clique na guia **Política de Voz**.</span><span class="sxs-lookup"><span data-stu-id="b898e-116">Click the **Voice Policy** tab.</span></span>

5.  <span data-ttu-id="b898e-117">Dê um duplo clique sobre uma política de voz existente para abrir a caixa de diálogo **Editar Política de Voz**.</span><span class="sxs-lookup"><span data-stu-id="b898e-117">Double-click an existing voice policy to open the **Edit Voice Policy** dialog box.</span></span>

6.  <span data-ttu-id="b898e-118">Em **Recursos de Chamadas**, selecione **Habilitar o estacionamento de chamadas**.</span><span class="sxs-lookup"><span data-stu-id="b898e-118">Under **Calling features**, select **Enable call park**.</span></span>

7.  <span data-ttu-id="b898e-119">Clique em **OK** para salvar a política de voz</span><span class="sxs-lookup"><span data-stu-id="b898e-119">Click **OK** to save the voice policy</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-enable-call-park-for-users"></a><span data-ttu-id="b898e-120">Para usar cmdlets para habilitar o estacionamento de chamadas para usuários</span><span class="sxs-lookup"><span data-stu-id="b898e-120">To Use Cmdlets to Enable Call Park for Users</span></span>

1.  <span data-ttu-id="b898e-121">Faça logon no computador como um membro do grupo RTCUniversalServerAdmins ou como um membro da função administrativa CsVoiceAdministrator, CsServerAdministrator ou CsAdministrator.</span><span class="sxs-lookup"><span data-stu-id="b898e-121">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator administrative role.</span></span>

2.  <span data-ttu-id="b898e-122">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="b898e-122">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="b898e-123">Execute:</span><span class="sxs-lookup"><span data-stu-id="b898e-123">Run:</span></span>
    
        Set-CsVoicePolicy -Identity <VoicePolicy> -EnableCallPark $true
    
    <span data-ttu-id="b898e-124">Por exemplo, para habilitar o estacionamento de chamadas para a política de voz global padrão:</span><span class="sxs-lookup"><span data-stu-id="b898e-124">For example, to enable Call Park for the default global voice policy:</span></span>
    
        Set-CsVoicePolicy -EnableCallPark $true

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b898e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b898e-125">See Also</span></span>


[<span data-ttu-id="b898e-126">Criar uma política de voz e configurar registros de uso de PSTN no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b898e-126">Create a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)  
  

<span data-ttu-id="b898e-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b898e-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

