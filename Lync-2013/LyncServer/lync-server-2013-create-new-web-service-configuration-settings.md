---
title: 'Lync Server 2013: criar novas definições de configuração de serviço Web'
description: 'Lync Server 2013: criar novas configurações de serviço Web.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create new Web Service configuration settings
ms:assetid: f3f04d81-8a1f-427f-bd0f-fb659024e096
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182605(v=OCS.15)
ms:contentKeyID: 48185801
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc66b0c8f394260fbe30e444f800640c774b6bcf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431887"
---
# <a name="create-new-web-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="b9919-103">Criar novas opções de configuração de serviço Web no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b9919-103">Create new Web Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b9919-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b9919-104">

<span> </span></span></span>

<span data-ttu-id="b9919-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="b9919-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="b9919-106">Você pode usar a página **serviço Web** para configurar os métodos de autenticação para acessar servidores Web relacionados ao Lync Server 2013 e serviços Web.</span><span class="sxs-lookup"><span data-stu-id="b9919-106">You can use the **Web Service** page to configure the authentication methods for accessing Lync Server 2013 related web servers and Web Services.</span></span>

<span data-ttu-id="b9919-107">Siga estas etapas para criar a nova política de Web Service.</span><span class="sxs-lookup"><span data-stu-id="b9919-107">Follow these steps to create a new Web Service policy.</span></span>

<div>

## <a name="to-create-new-web-service-configuration-settings"></a><span data-ttu-id="b9919-108">Para criar novas definições de configuração de serviço da Web</span><span class="sxs-lookup"><span data-stu-id="b9919-108">To create new web service configuration settings</span></span>

1.  <span data-ttu-id="b9919-109">Em uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes) ou atribuído à função CsServerAdministrator ou CsAdministrator, faça logon em qualquer computador que esteja na rede na qual você implantou o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b9919-109">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="b9919-110">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="b9919-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="b9919-111">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b9919-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="b9919-112">Na barra de navegação esquerda, clique em **Segurança** e em **Serviço da Web**.</span><span class="sxs-lookup"><span data-stu-id="b9919-112">In the left navigation bar, click **Security** and then click **Web Service**.</span></span>

4.  <span data-ttu-id="b9919-113">Na página **Serviço da Web**, clique em **Novo** e faça um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="b9919-113">On the **Web Service** page, click **New**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="b9919-p102">Para configurar o Serviço da Web para um site, clique em **Configuração do site**. Em **Selecionar um site**, clique em um site no qual a política de Serviço da Web será aplicada e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9919-p102">To configure the Web Service for a site, click **Site configuration**. In **Select a Site**, click the site to which the Web Service policy will be applied a site and click **OK**.</span></span>
    
      - <span data-ttu-id="b9919-p103">Para configurar o Serviço da Web para um pool, clique em **Configuração do pool**. Em **Selecionar um Serviço**, clique no serviço no qual a política de Serviço da Web será aplicada e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9919-p103">To configure the Web Service for a pool, click **Pool configuration**. In **Select a Service**, click the service to which the Web Service policy will be applied and click **OK**.</span></span>

5.  <span data-ttu-id="b9919-118">Em **Nova configuração do Serviço da Web**, em **Autenticação integrada do Windows**, selecione **Negociar**, **Autenticação integrada do Windows** ou **Nenhum**.</span><span class="sxs-lookup"><span data-stu-id="b9919-118">In **New Web Service Setting**, in **Integrated Windows authentication**, select **Negotiate**, **Integrated Windows authentication**, or **None**.</span></span>

6.  <span data-ttu-id="b9919-119">Selecione um ou mais dos seguintes dependendo das capacidades dos clientes e do suporte no seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="b9919-119">Select one or more of the following depending on the capabilities of the clients and support in your environment:</span></span>
    
      - <span data-ttu-id="b9919-120">**Habilitar autenticação de PIN** para permitir que os clientes sejam autenticados usando números PIN.</span><span class="sxs-lookup"><span data-stu-id="b9919-120">**Enable PIN Authentication** to enable clients to be authenticated using PIN numbers.</span></span>
    
      - <span data-ttu-id="b9919-121">**Habilitar autenticação de certificado** para que os servidores no pool emitam certificados para os clientes.</span><span class="sxs-lookup"><span data-stu-id="b9919-121">**Enable certificate authentication** to have the servers in the pool issue certificates to clients.</span></span>
    
      - <span data-ttu-id="b9919-122">**Habilitar download da cadeia de certificados** para que os servidores sejam apresentados com um download de certificado de autenticação da cadeia de certificados para aquele certificado.</span><span class="sxs-lookup"><span data-stu-id="b9919-122">**Enable certificate chain download** to have servers presented with an authentication certificate download the certificate chain for that certificate.</span></span>

7.  <span data-ttu-id="b9919-123">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="b9919-123">Click **Commit**.</span></span>

<span data-ttu-id="b9919-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b9919-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

