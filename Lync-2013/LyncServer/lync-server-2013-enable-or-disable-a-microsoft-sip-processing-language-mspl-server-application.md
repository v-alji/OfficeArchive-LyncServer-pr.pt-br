---
title: 'Lync Server 2013: habilitar ou desabilitar um aplicativo de servidor Microsoft SIP Processing Language (MSPL)'
description: 'Lync Server 2013: habilitar ou desabilitar um aplicativo de servidor Microsoft SIP Processing Language (MSPL).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable a Microsoft SIP Processing Language (MSPL) server application
ms:assetid: b20af38d-224a-4459-991d-0b7eabb3ca7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182573(v=OCS.15)
ms:contentKeyID: 48185145
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8f919599d6c6a39fea73424f4e287f00636c0982
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389884"
---
# <a name="enable-or-disable-a-microsoft-sip-processing-language-mspl-server-application-in-lync-server-2013"></a><span data-ttu-id="8350f-103">Habilitar ou desabilitar um aplicativo de servidor Microsoft SIP Processing Language (MSPL) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8350f-103">Enable or disable a Microsoft SIP Processing Language (MSPL) server application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8350f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8350f-104">

<span> </span></span></span>

<span data-ttu-id="8350f-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="8350f-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="8350f-106">Você pode usar o painel de controle do Lync Server para habilitar ou desabilitar aplicativos do servidor Microsoft SIP Processing Language (MSPL) que são executados em seu ambiente do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8350f-106">You can use Lync Server Control Panel to enable or disable Microsoft SIP Processing Language (MSPL) server applications that run in your Lync Server 2013 environment.</span></span> <span data-ttu-id="8350f-107">Esses aplicativos são aplicativos somente de script que usam uma linguagem de script em vez da API do Microsoft Lync 2013 Preview.</span><span class="sxs-lookup"><span data-stu-id="8350f-107">These applications are script-only applications that use a scripting language instead of the Microsoft Lync 2013 Preview API.</span></span>

<span data-ttu-id="8350f-108">Nem todos os scripts podem ser habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="8350f-108">Not all scripts can be enabled or disabled.</span></span> <span data-ttu-id="8350f-109">Por exemplo, o script defaultrouting está habilitado e essa opção não pode ser alterada para defaultrouting.</span><span class="sxs-lookup"><span data-stu-id="8350f-109">For instance, the DefaultRouting script is enabled and this option cannot be changed for DefaultRouting.</span></span>

<div>

## <a name="to-enable-or-disable-an-mspl-server-application"></a><span data-ttu-id="8350f-110">Para habilitar ou desabilitar um aplicativo de servidor MSPL</span><span class="sxs-lookup"><span data-stu-id="8350f-110">To enable or disable an MSPL server application</span></span>

1.  <span data-ttu-id="8350f-111">Em uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes) ou atribuído à função CsServerAdministrator ou CsAdministrator, faça logon em qualquer computador que esteja na rede na qual você implantou o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8350f-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="8350f-112">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="8350f-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8350f-113">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8350f-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8350f-114">Na barra de navegação à esquerda, clique em **topologia** e, em seguida, clique em **aplicativo para servidor**.</span><span class="sxs-lookup"><span data-stu-id="8350f-114">In the left navigation bar, click **Topology** and then click **Server Application**.</span></span>

4.  <span data-ttu-id="8350f-115">Na página **aplicativo do servidor** , clique em um título de coluna para classificar os aplicativos, se necessário, e clique no aplicativo servidor que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="8350f-115">On the **Server Application** page, click a column heading to sort the applications, if needed, and then click the server application that you want to modify.</span></span>

5.  <span data-ttu-id="8350f-116">Clique em **ação**.</span><span class="sxs-lookup"><span data-stu-id="8350f-116">Click **Action**.</span></span>

6.  <span data-ttu-id="8350f-117">Clique em **habilitar aplicativo** ou em **desabilitar aplicativo** (ou seja, se o script der suporte a essa opção).</span><span class="sxs-lookup"><span data-stu-id="8350f-117">Click **Enable application** or **Disable application** (that is, if the script supports this option).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8350f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8350f-118">See Also</span></span>


[<span data-ttu-id="8350f-119">Marcar um aplicativo Microsoft SIP Processing Language (MSPL) como crítico ou não crítico no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8350f-119">Mark a Microsoft SIP Processing Language (MSPL) application as critical or not critical in Lync Server 2013</span></span>](lync-server-2013-mark-a-microsoft-sip-processing-language-mspl-application-as-critical-or-not-critical.md)  


[<span data-ttu-id="8350f-120">Exibir aplicativos de servidor do Idioma de Processamento SIP da Microsoft (MSPL) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8350f-120">View Microsoft SIP Processing Language (MSPL) server applications in Lync Server 2013</span></span>](lync-server-2013-view-microsoft-sip-processing-language-mspl-server-applications.md)  


[<span data-ttu-id="8350f-121">Gerenciando a topologia do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8350f-121">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="8350f-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8350f-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

