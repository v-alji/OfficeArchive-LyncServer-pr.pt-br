---
title: 'Lync Server 2013: excluir configurações de configuração de serviço Web existentes'
description: 'Lync Server 2013: excluir as configurações de configuração de serviço Web existentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete existing Web Service configuration settings
ms:assetid: c2b96f4c-4b07-48e6-9ca6-55bc0e0cf5a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182582(v=OCS.15)
ms:contentKeyID: 48185333
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5a28197f26a447112e29b6e4a831585dd49a9854
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430438"
---
# <a name="delete-existing-web-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="ffacd-103">Excluir as configurações de configuração de serviço Web existentes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ffacd-103">Delete existing Web Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ffacd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ffacd-104">

<span> </span></span></span>

<span data-ttu-id="ffacd-105">_**Tópico da última modificação:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ffacd-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ffacd-106">Siga estas etapas para excluir definições de configuração do serviço da web.</span><span class="sxs-lookup"><span data-stu-id="ffacd-106">Follow these steps to delete web service configuration settings.</span></span>

<div>

## <a name="to-delete-web-service-configuration-settings"></a><span data-ttu-id="ffacd-107">Para excluir definições de configuração de serviço da Web</span><span class="sxs-lookup"><span data-stu-id="ffacd-107">To delete web service configuration settings</span></span>

1.  <span data-ttu-id="ffacd-108">Em uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes) ou atribuído à função CsServerAdministrator ou CsAdministrator, faça logon em qualquer computador que esteja na rede na qual você implantou o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ffacd-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="ffacd-109">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="ffacd-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ffacd-110">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ffacd-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ffacd-111">Na barra de navegação esquerda, clique em **Segurança** e em **Serviço da Web**.</span><span class="sxs-lookup"><span data-stu-id="ffacd-111">In the left navigation bar, click **Security** and then click **Web Service**.</span></span>

4.  <span data-ttu-id="ffacd-112">Na página **Serviço da Web**, e no campo de pesquisa, digite todo ou parte do nome da política que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="ffacd-112">On the **Web Service** page, and in the search field, type all or part of the name of the policy you want to delete.</span></span>

5.  <span data-ttu-id="ffacd-113">Na lista de políticas, clique na política que você deseja, clique em **Editar** e em **Excluir**.</span><span class="sxs-lookup"><span data-stu-id="ffacd-113">In the list of policies, click the policy that you want, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="ffacd-114">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffacd-114">Click **OK**.</span></span>

</div>

<div>

## <a name="deleting-web-service-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ffacd-115">Excluindo configurações de serviço Web usando cmdlets do Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ffacd-115">Deleting Web Service Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ffacd-116">Você pode excluir as configurações de serviço Web usando o Windows PowerShell e o cmdlet **Remove-CsWebServiceConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="ffacd-116">You can delete web service configuration settings by using Windows PowerShell and the **Remove-CsWebServiceConfiguration** cmdlet.</span></span> <span data-ttu-id="ffacd-117">Você pode executar esse cmdlet a partir do Shell de gerenciamento do Lync Server 2013 ou de uma sessão remota do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ffacd-117">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ffacd-118">Para obter detalhes sobre como usar o Windows PowerShell remoto para se conectar ao Lync Server, consulte o artigo sobre o blog do Windows PowerShell do Lync Server "início rápido: gerenciar o Microsoft Lync Server 2010 usando o PowerShell remoto" em [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="ffacd-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-delete-a-specific-collection-of-web-service-configuration-settings"></a><span data-ttu-id="ffacd-119">Para excluir um conjunto específico de definições de configuração do serviço da Web</span><span class="sxs-lookup"><span data-stu-id="ffacd-119">To delete a specific collection of web service configuration settings</span></span>

  - <span data-ttu-id="ffacd-120">O seguinte comando remove as configurações de segurança do Serviço da Web aplicadas ao local Redmond:</span><span class="sxs-lookup"><span data-stu-id="ffacd-120">The following command removes the Web Service security settings applied to the Redmond site:</span></span>
    
        Remove-CsWebServiceConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-delete-all-of-the-web-service-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="ffacd-121">Para excluir todas as definições de configuração do serviço da Web aplicadas ao escopo local</span><span class="sxs-lookup"><span data-stu-id="ffacd-121">To delete all of the web service configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="ffacd-122">O seguinte comando remove todas as configurações de segurança do Serviço da Web aplicadas ao escopo do serviço:</span><span class="sxs-lookup"><span data-stu-id="ffacd-122">The following command removes all of the Web Service security settings applied to the service scope:</span></span>
    
        Get-CsWebServiceConfiguration -Filter "service:*" | Remove-CsWebServiceConfiguration

</div>

<div>

## <a name="to-delete-all-of-the-web-service-configuration-settings-that-allow-certificate-authentication"></a><span data-ttu-id="ffacd-123">Para excluir todas as definições de configuração do Serviço da Web que permitem a autenticação de certificado</span><span class="sxs-lookup"><span data-stu-id="ffacd-123">To delete all of the web service configuration settings that allow certificate authentication</span></span>

  - <span data-ttu-id="ffacd-124">O seguinte comando remove todas as configurações de segurança do Serviço da Web que permitem o uso de autenticação de certificados:</span><span class="sxs-lookup"><span data-stu-id="ffacd-124">The following command removes all the Web Service security settings that allow the use of certificate authentication:</span></span>
    
        Get-CsWebServiceConfiguration | Where-Object {$_.UseCertificateAuth -eq $True} | Remove-CsWebServiceConfiguration

</div>

<span data-ttu-id="ffacd-125">Para obter detalhes, consulte [Remove-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsWebServiceConfiguration).</span><span class="sxs-lookup"><span data-stu-id="ffacd-125">For details, see [Remove-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsWebServiceConfiguration).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ffacd-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffacd-126">See Also</span></span>


[<span data-ttu-id="ffacd-127">Configurando autenticação no painel de controle do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ffacd-127">Configuring authentication in the Lync Server 2013 Control Panel</span></span>](lync-server-2013-configuring-authentication-in-the-lync-server-control-panel.md)  
  

<span data-ttu-id="ffacd-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ffacd-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

