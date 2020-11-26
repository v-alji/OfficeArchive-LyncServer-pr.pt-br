---
title: 'Lync Server 2013: exibir informações sobre as configurações de notificação por push'
description: 'Lync Server 2013: exibir informações sobre as configurações de notificação por push.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing information about push notification settings
ms:assetid: be5c6b01-4294-4d17-9772-fed40201e8a5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721868(v=OCS.15)
ms:contentKeyID: 49733801
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44ee876df341833c93e97fd16664940629754a6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443976"
---
# <a name="viewing-information-about-push-notification-settings-in-lync-server-2013"></a><span data-ttu-id="dbd9b-103">Exibir informações sobre as configurações de notificação por push no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbd9b-103">Viewing information about push notification settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dbd9b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dbd9b-104">

<span> </span></span></span>

<span data-ttu-id="dbd9b-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="dbd9b-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="dbd9b-106">As notificações por push, na forma de selos, ícones ou alertas, podem ser enviadas para um dispositivo móvel mesmo quando o aplicativo móvel estiver inativo.</span><span class="sxs-lookup"><span data-stu-id="dbd9b-106">Push notifications, in the form of badges, icons, or alerts, can be sent to a mobile device even when the mobile application is inactive.</span></span> <span data-ttu-id="dbd9b-107">As notificações por push notificam um usuário de eventos como um convite de mensagem instantânea novo ou perdido e caixa postal.</span><span class="sxs-lookup"><span data-stu-id="dbd9b-107">Push notifications notify a user of events such as a new or missed IM invitation and voice mail.</span></span> <span data-ttu-id="dbd9b-108">Você pode visualizar as configurações de notificações por push de informações para dispositivos móveis usando o painel de controle do Lync Server 2013 ou o Shell de gerenciamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dbd9b-108">You can view information push notifications settings for mobile devices by using either Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-view-push-notification-information-from-lync-server-control-panel"></a><span data-ttu-id="dbd9b-109">Para exibir as informações de notificação por push no painel de controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="dbd9b-109">To view push notification information from Lync Server Control Panel</span></span>

1.  <span data-ttu-id="dbd9b-110">Usando uma conta de usuário atribuída à função CsUserAdministrator ou CsAdministrator, faça logon em qualquer computador de sua implantação interna.</span><span class="sxs-lookup"><span data-stu-id="dbd9b-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="dbd9b-111">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="dbd9b-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="dbd9b-112">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="dbd9b-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="dbd9b-113">Na barra de navegação à esquerda, clique em **clientes** e, em seguida, clique no botão de navegação **configuração por push de notificação** .</span><span class="sxs-lookup"><span data-stu-id="dbd9b-113">In the left navigation bar, click **Clients**, and then click the **Push Notification Configuration** navigation button.</span></span>

4.  <span data-ttu-id="dbd9b-114">Na página **configuração de notificação por push** , clique no site que você deseja exibir, clique no menu **Editar** e, em seguida, clique em **Mostrar detalhes**.</span><span class="sxs-lookup"><span data-stu-id="dbd9b-114">On the **Push Notification Configuration** page, click the site you want to view, click the **Edit** menu, and then click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-push-notification-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="dbd9b-115">Exibir informações de notificação por push usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dbd9b-115">Viewing Push Notification Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="dbd9b-116">Você pode exibir as configurações de notificação por push usando o Windows PowerShell e o cmdlet **Get-CsPushNotificationConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="dbd9b-116">You can view push notification configuration settings by using Windows PowerShell and the **Get-CsPushNotificationConfiguration** cmdlet.</span></span> <span data-ttu-id="dbd9b-117">Você pode executar esse cmdlet a partir do Shell de gerenciamento do Lync Server 2013 ou de uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dbd9b-117">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="dbd9b-118">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="dbd9b-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-push-notification-configuration-information"></a><span data-ttu-id="dbd9b-119">Para exibir informações de configuração de notificação por push</span><span class="sxs-lookup"><span data-stu-id="dbd9b-119">To view push notification configuration information</span></span>

  - <span data-ttu-id="dbd9b-120">Para ver as informações sobre todas as suas configurações de notificação por push, digite o seguinte comando no Shell de gerenciamento do Lync Server e pressione ENTER:</span><span class="sxs-lookup"><span data-stu-id="dbd9b-120">To view information about all your push notification configuration settings, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsPushNotificationConfiguration
    
    <span data-ttu-id="dbd9b-121">Isso retornará informações parecidas com:</span><span class="sxs-lookup"><span data-stu-id="dbd9b-121">That will return information similar to this:</span></span>
    
        Identity                               : Global
        EnableApplePushNotificationService     : False
        EnableMicrosoftPushNotificationService : False

</div>

<span data-ttu-id="dbd9b-122">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [Get-CsPushNotificationConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsPushNotificationConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="dbd9b-122">For more information, see the help topic for the [Get-CsPushNotificationConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsPushNotificationConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="dbd9b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbd9b-123">See Also</span></span>


[<span data-ttu-id="dbd9b-124">Configurando notificações por push no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbd9b-124">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)  
  

<span data-ttu-id="dbd9b-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dbd9b-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

