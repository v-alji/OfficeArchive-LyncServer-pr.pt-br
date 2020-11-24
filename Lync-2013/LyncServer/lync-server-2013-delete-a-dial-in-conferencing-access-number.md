---
title: 'Lync Server 2013: excluir um número de acesso à conferência discada'
description: 'Lync Server 2013: excluir um número de acesso à conferência discada.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a dial-in conferencing access number
ms:assetid: 199c5d9c-0489-4ad5-a7f1-ca59fe0e6ac7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520956(v=OCS.15)
ms:contentKeyID: 48183522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa5bed6099f7464884c3bcde8e4ee86ad4207222
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390345"
---
# <a name="delete-a-dial-in-conferencing-access-number-in-lync-server-2013"></a><span data-ttu-id="f9671-103">Excluir um número de acesso à conferência discada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9671-103">Delete a dial-in conferencing access number in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9671-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9671-104">

<span> </span></span></span>

<span data-ttu-id="f9671-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="f9671-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="f9671-106">Siga estas etapas para excluir um número de acesso à conferência discada.</span><span class="sxs-lookup"><span data-stu-id="f9671-106">Follow these steps to delete a dial-in conferencing access number.</span></span>

<div>

## <a name="to-delete-a-dial-in-conferencing-access-number"></a><span data-ttu-id="f9671-107">Para excluir um número de acesso à conferência discada</span><span class="sxs-lookup"><span data-stu-id="f9671-107">To delete a dial-in conferencing access number</span></span>

1.  <span data-ttu-id="f9671-108">Em uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes) ou atribuído à função CsServerAdministrator ou CsAdministrator, faça logon em qualquer computador que esteja na rede na qual você implantou o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f9671-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="f9671-109">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f9671-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f9671-110">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f9671-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f9671-111">Na barra de navegação à esquerda, clique em **Conferência** e, então, em  **Número de acesso de discagem**.</span><span class="sxs-lookup"><span data-stu-id="f9671-111">In the left navigation bar, click **Conferencing**, and then click **Dial-in Access Number**.</span></span>

4.  <span data-ttu-id="f9671-112">Na página, clique no número de discagem que deseja excluir da lista, clique em  **Editar** e, em seguida, clique em **Excluir**.</span><span class="sxs-lookup"><span data-stu-id="f9671-112">On the page, click the dial-in number you want to delete in the list, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="f9671-113">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9671-113">Click **OK**.</span></span>

</div>

<div>

## <a name="removing-dial-in-conferencing-access-numbers-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="f9671-114">Removendo números de acesso à conferência discada usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9671-114">Removing Dial-in Conferencing Access Numbers by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="f9671-115">Os números de acesso à conferência discada podem ser excluídos usando-se o Windows PowerShell e o cmdlet **Remove-CsDialInConferencingAccessNumber** .</span><span class="sxs-lookup"><span data-stu-id="f9671-115">Dial-in conferencing access numbers can be deleted by using Windows PowerShell and the **Remove-CsDialInConferencingAccessNumber** cmdlet.</span></span> <span data-ttu-id="f9671-116">Esse cmdlet pode ser executado no Shell de gerenciamento do Lync Server 2013 ou em uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f9671-116">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="f9671-117">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="f9671-117">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specific-dial-in-conferencing-access-number"></a><span data-ttu-id="f9671-118">Para remover um número de acesso de conferência discada específico</span><span class="sxs-lookup"><span data-stu-id="f9671-118">To remove a specific dial-in conferencing access number</span></span>

  - <span data-ttu-id="f9671-119">Esse comando exclui o número de acesso à conferência discada com identidade sip:RedmondDialInAccess@litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="f9671-119">This command deletes the dial-in conferencing access number with Identity sip:RedmondDialInAccess@litwareinc.com:</span></span>
    
        Remove-CsDialInConferencingAccessNumber -Identity "sip:RedmondDialInAccess@litwareinc.com"

</div>

<div>

## <a name="to-remove-all-the-dial-in-conferencing-access-numbers-assigned-to-a-specific-region"></a><span data-ttu-id="f9671-120">Para remover todos os números de acesso à conferência discada atribuídos a uma região específica</span><span class="sxs-lookup"><span data-stu-id="f9671-120">To remove all the dial-in conferencing access numbers assigned to a specific region</span></span>

  - <span data-ttu-id="f9671-121">Esse comando exclui todos os números de acesso à conferência discada associados à região noroeste:</span><span class="sxs-lookup"><span data-stu-id="f9671-121">This command deletes all the dial-in conferencing access numbers associated with the Northwest region:</span></span>
    
        Get-CsDialInConferencingAccessNumber -Region "Northwest" | Remove-CsDialInConferencingAccessNumber

</div>

<div>

## <a name="to-remove-dial-in-conferencing-access-numbers-based-on-primary-language"></a><span data-ttu-id="f9671-122">Para remover números de acesso à conferência discada com base no idioma principal</span><span class="sxs-lookup"><span data-stu-id="f9671-122">To remove dial-in conferencing access numbers based on primary language</span></span>

  - <span data-ttu-id="f9671-123">Esse comando exclui todos os números de acesso à conferência discada em que a italiano é o idioma principal:</span><span class="sxs-lookup"><span data-stu-id="f9671-123">This command deletes all the dial-in conferencing access numbers where Italian is the primary language:</span></span>
    
        Get-CsDialInConferencingAccessNumber | Where-Object {$_.PrimaryLanguage -eq "it-IT"} | Remove-CsDialInConferencingAccessNumber

</div>

<span data-ttu-id="f9671-124">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [Remove-CsDialInConferencingAccessNumber](https://docs.microsoft.com/powershell/module/skype/Remove-CsDialInConferencingAccessNumber) .</span><span class="sxs-lookup"><span data-stu-id="f9671-124">For more information, see the help topic for the [Remove-CsDialInConferencingAccessNumber](https://docs.microsoft.com/powershell/module/skype/Remove-CsDialInConferencingAccessNumber) cmdlet.</span></span>

<span data-ttu-id="f9671-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9671-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

