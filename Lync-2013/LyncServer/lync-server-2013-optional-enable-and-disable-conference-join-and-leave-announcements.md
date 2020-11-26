---
title: (Opcional) Habilitar e desabilitar comunicados de ingresso e saída de conferência
description: Adicionais Habilitar e desabilitar o ingresso em conferência e deixar anúncios.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Enable and disable conference join and leave announcements
ms:assetid: c9529568-e66c-48d8-aef2-9072f9c336ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398834(v=OCS.15)
ms:contentKeyID: 48185403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 70cd6b452a44d7d40f23d5ca96b6e4b7b063d2ec
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445236"
---
# <a name="optional-enable-and-disable-conference-join-and-leave-announcements-in-lync-server-2013"></a><span data-ttu-id="8794c-103">(Opcional) Habilitar e desabilitar comunicados de ingresso e saída de conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8794c-103">(Optional) Enable and disable conference join and leave announcements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8794c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8794c-104">

<span> </span></span></span>

<span data-ttu-id="8794c-105">_**Tópico da última modificação:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="8794c-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="8794c-106">Quando os usuários de discagem entram ou deixam uma conferência, o aplicativo de anúncio de conferência pode anunciar a entrada ou a saída tocando um tom ou dizendo seus nomes.</span><span class="sxs-lookup"><span data-stu-id="8794c-106">When dial-in users join or leave a conference, the Conferencing Announcement application can announce their entrance or exit by playing a tone or saying their names.</span></span> <span data-ttu-id="8794c-107">Você pode alterar como os comunicados funcionam Executando cmdlets.</span><span class="sxs-lookup"><span data-stu-id="8794c-107">You can change how announcements work by running cmdlets.</span></span> <span data-ttu-id="8794c-108">Esta etapa é opcional.</span><span class="sxs-lookup"><span data-stu-id="8794c-108">This step is optional.</span></span>

<div>

## <a name="to-modify-the-conference-join-and-leave-announcement-behavior"></a><span data-ttu-id="8794c-109">Para modificar o comportamento de anúncio de ingresso e saída de conferência</span><span class="sxs-lookup"><span data-stu-id="8794c-109">To modify the conference join and leave announcement behavior</span></span>

1.  <span data-ttu-id="8794c-110">Faça logon no computador como membro do grupo RTCUniversalServerAdmins ou como membro da função **cs-ServerAdministrator** ou **CsAdministrator** .</span><span class="sxs-lookup"><span data-stu-id="8794c-110">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="8794c-111">Inicie o Shell de gerenciamento do Lync Server: clique em **Iniciar**, em **todos os programas**, em **Microsoft Lync Server 2013** e, em seguida, clique em **Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="8794c-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="8794c-112">Execute o seguinte no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="8794c-112">Run the following at the command prompt:</span></span>
    
        Get-CsDialinConferencingConfiguration
    
    <span data-ttu-id="8794c-113">Esse cmdlet recupera informações sobre a necessidade de os participantes gravarem o nome ao ingressar em uma conferência e como o Lync Server responde quando os participantes ingressam ou deixam uma conferência discada.</span><span class="sxs-lookup"><span data-stu-id="8794c-113">This cmdlet retrieves information about whether participants are required to record their name when joining a conference and how Lync Server responds when participants join or leave a dial-in conference.</span></span>

4.  <span data-ttu-id="8794c-114">Execute o seguinte no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="8794c-114">Run the following at the command prompt:</span></span>
    
        Set-CsDialinConferencingConfiguration -Identity <identity of dial-in conferencing settings to be modified>
        [-EnableNameRecording <$true | $false>]
        [-EntryExitAnnouncementsEnabledByDefault <$true | $false>]
        [-EntryExitAnnouncementsType <UseNames | ToneOnly]
    
    <span data-ttu-id="8794c-115">**EnableNameRecording**   Determina se os participantes anônimos são solicitados a gravar o nome antes de entrar na conferência.</span><span class="sxs-lookup"><span data-stu-id="8794c-115">**EnableNameRecording**   Determines whether anonymous participants are asked to record their name before entering the conference.</span></span> <span data-ttu-id="8794c-116">O valor padrão é "$true", que significa que os participantes receberão essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="8794c-116">The default value is "$true," which means that anonymous participants are prompted to state their name when joining a conference.</span></span> <span data-ttu-id="8794c-117">(Os participantes autenticados não registram seus nomes porque seu nome de exibição é utilizado.)</span><span class="sxs-lookup"><span data-stu-id="8794c-117">(Authenticated participants do not record their name because their display name is used instead.)</span></span>
    
    <span data-ttu-id="8794c-118">**EntryExitAnnouncementsEnabledByDefault**   Indica se os comunicados estão ativados ou desativados por padrão.</span><span class="sxs-lookup"><span data-stu-id="8794c-118">**EntryExitAnnouncementsEnabledByDefault**   Indicates whether announcements are turned on or off by default.</span></span> <span data-ttu-id="8794c-119">O valor padrão é "$false", o que significa que, por padrão, não há anúncios quando os participantes participam ou saem de uma conferência.</span><span class="sxs-lookup"><span data-stu-id="8794c-119">The default value is "$false," which means that by default there are no announcements when participants join or leave a conference.</span></span> <span data-ttu-id="8794c-120">O organizador da reunião pode substituir essa configuração ao agendar uma reunião.</span><span class="sxs-lookup"><span data-stu-id="8794c-120">The meeting organizer can override this setting when scheduling a meeting.</span></span>
    
    <span data-ttu-id="8794c-121">**EntryExitAnnouncementsType**   Indica a ação tomada sempre que um participante ingressa ou sai de uma conferência para a qual os comunicados são habilitados.</span><span class="sxs-lookup"><span data-stu-id="8794c-121">**EntryExitAnnouncementsType**   Indicates the action taken whenever a participant joins or leaves a conference for which announcements are enabled.</span></span> <span data-ttu-id="8794c-122">O valor padrão é "UseNames", que significa que há um anúncio parecido com o seguinte: "Ken Myer está participando da conferência" quando os anúncios são ativados.</span><span class="sxs-lookup"><span data-stu-id="8794c-122">The default value is "UseNames," which means there is an announcement similar to the following: "Ken Myer has joined the conference" when announcements are turned on.</span></span>
    
    <span data-ttu-id="8794c-p105">É possível definir essas configurações no escopo global ou no escopo do site. As configurações definidas no escopo do site têm precedência sobre as configurações definidas no escopo global.</span><span class="sxs-lookup"><span data-stu-id="8794c-p105">You can configure these settings at the global scope or at the site scope. Settings configured at the site scope take precedence over settings configured at the global scope.</span></span>
    
    <span data-ttu-id="8794c-125">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8794c-125">For example:</span></span>
    
        Set-CsDialinConferencingConfiguration -Identity site:Redmond
        -EnableNameRecording $false
        -EntryExitAnnouncementsEnabledByDefault $true
        -EntryExitAnnouncementsType ToneOnly
    
    <span data-ttu-id="8794c-126">Neste exemplo, as configurações são configuradas no escopo do site de Redmond.</span><span class="sxs-lookup"><span data-stu-id="8794c-126">In this example, settings are configured at the site scope for Redmond.</span></span> <span data-ttu-id="8794c-127">Os anúncios estão ativados, mas os participantes não recebem uma solicitação para inserir seus nomes quando ingressam em uma conferência.</span><span class="sxs-lookup"><span data-stu-id="8794c-127">Announcements are turned on, but participants are not prompted to say their name when they join a conference.</span></span> <span data-ttu-id="8794c-128">Um tom é tocado quando os participantes entram ou deixam uma conferência.</span><span class="sxs-lookup"><span data-stu-id="8794c-128">A tone is played when participants enter or leave a conference.</span></span>

<span data-ttu-id="8794c-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8794c-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

