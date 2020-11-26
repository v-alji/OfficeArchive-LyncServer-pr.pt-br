---
title: 'Lync Server 2013: Instalando o portal da Web administrativo do sistema de salas do Lync'
description: 'Lync Server 2013: Instalando o portal da Web administrativo do sistema de salas do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Lync Room System Administrative Web Portal
ms:assetid: dd19e368-c338-4e21-a40d-6439d46a9748
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436326(v=OCS.15)
ms:contentKeyID: 56737622
ms.date: 04/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0fba239346d75142bb4009c58e0ac67e8e1f3bcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427002"
---
# <a name="installing-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a><span data-ttu-id="99325-103">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="99325-103">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99325-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99325-104">

<span> </span></span></span>

<span data-ttu-id="99325-105">_**Tópico da última modificação:** 2015-04-09_</span><span class="sxs-lookup"><span data-stu-id="99325-105">_**Topic Last Modified:** 2015-04-09_</span></span>

<span data-ttu-id="99325-106">Você pode baixar o portal da Web administrativo do sistema de sala do Microsoft Lync no centro de download da Microsoft em [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044) .</span><span class="sxs-lookup"><span data-stu-id="99325-106">You can download the Microsoft Lync Room System Administrative Web Portal from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044).</span></span>

<span data-ttu-id="99325-107">Para instalar o portal da Web administrativo do sistema de salas do Lync, use as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="99325-107">To install the Lync Room System Administrative Web Portal, use the following steps.</span></span>

1.  <span data-ttu-id="99325-108">Configure a porta de aplicativo confiável executando o seguinte cmdlet no Shell de gerenciamento do Lync Server:</span><span class="sxs-lookup"><span data-stu-id="99325-108">Configure the Trusted Application Port by running the following cmdlet in Lync Server Management Shell:</span></span>
    
        Set-CsWebServer -Identity POOLFQDN -MeetingRoomAdminPortalInternalListeningPort 4456 -MeetingRoomAdminPortalExternalListeningPort 4457

2.  <span data-ttu-id="99325-109">Para instalar o portal de sala de reunião, baixe **LyncRoomAdminPortal.exe** e, em seguida, execute-o como administrador.</span><span class="sxs-lookup"><span data-stu-id="99325-109">To install the Meeting Room Portal, download **LyncRoomAdminPortal.exe** and then run it as an administrator.</span></span>

3.  <span data-ttu-id="99325-110">Abra o arquivo Web.config do seguinte local:</span><span class="sxs-lookup"><span data-stu-id="99325-110">Open the Web.config file from the following location:</span></span>
    
    <span data-ttu-id="99325-111">% Arquivos de programa% \\ Microsoft Lync Server 2013 \\ Web Components do \\ portal de sala de reunião do portal de sala de reunião \\ </span><span class="sxs-lookup"><span data-stu-id="99325-111">%Program Files%\\Microsoft Lync Server 2013\\Web Components\\Meeting Room Portal\\Int\\Handler</span></span>\\\\

4.  <span data-ttu-id="99325-112">No arquivo Web.Config, altere o PortalUserName para o nome de usuário criado na etapa 2 na seção "Configurando pré-requisitos para o portal de administração do sistema de salas do Lync" (o nome recomendado na etapa é LRSApp):</span><span class="sxs-lookup"><span data-stu-id="99325-112">In the Web.Config file, change the PortalUserName to the username created in Step 2 under the section “Configuring Prerequisites for Lync Room System Admin Portal” (the recommended name in the step is LRSApp):</span></span>
    
        <add key="PortalUserName" value="sip:LRSApp@domain.com" />

5.  <span data-ttu-id="99325-113">Como o portal de administração do LRS é um aplicativo confiável, você não precisa fornecer a senha na configuração do Portal.</span><span class="sxs-lookup"><span data-stu-id="99325-113">Because the LRS Admin Portal is a trusted application, you do not need to provide the password in the portal configuration.</span></span> <span data-ttu-id="99325-114">Se este usuário estiver usando um registrador diferente do registrador local, você precisará especificar o registrador para ele adicionando a seguinte linha no arquivo Web.Config:</span><span class="sxs-lookup"><span data-stu-id="99325-114">If this user is using a different registrar than local registrar, you need to specify the registrar for it by adding the following line in the Web.Config file:</span></span>
    
        <add key="PortalUserRegistrarFQDN" value="pool-xxxx.domain.com" />

6.  <span data-ttu-id="99325-115">Se a porta usada for diferente de 5061, adicione a seguinte linha no arquivo Web.Config:</span><span class="sxs-lookup"><span data-stu-id="99325-115">If the port used is other than 5061, add the following line in the Web.Config file:</span></span>
    
        <add key="PortalUserRegistrarPort" value="5061" />

<div>

## <a name="verifying-installation-of-the-lync-room-system-administrative-web-portal"></a><span data-ttu-id="99325-116">Verificando a instalação do portal da Web administrativo do sistema de salas do Lync</span><span class="sxs-lookup"><span data-stu-id="99325-116">Verifying Installation of the Lync Room System Administrative Web Portal</span></span>

<span data-ttu-id="99325-117">Para verificar a instalação do portal da Web administrativo do sistema de salas do Lync, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="99325-117">To verify installation of the Lync Room System Administrative Web Portal, do the following:</span></span>


1.  <span data-ttu-id="99325-118">Em um servidor front-end, navegue até a seguinte URL:</span><span class="sxs-lookup"><span data-stu-id="99325-118">On a Front End server, browse to the following URL:</span></span>
    
    <span data-ttu-id="99325-119"> https:// \<fe-server\> /lRS</span><span class="sxs-lookup"><span data-stu-id="99325-119">https://\<fe-server\>/lrs</span></span>
    
    <span data-ttu-id="99325-120">Você não verá nenhum erro, conforme mostrado na imagem a seguir:</span><span class="sxs-lookup"><span data-stu-id="99325-120">You should not see any errors, as shown in the following image:</span></span>
    
    <span data-ttu-id="99325-121">![Tela de entrada do portal de administração do sistema de salas do Lync](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Tela de entrada do portal de administração do sistema de salas do Lync")</span><span class="sxs-lookup"><span data-stu-id="99325-121">![Lync Room System Admin Portal Sign In screen](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync Room System Admin Portal Sign In screen")</span></span>

2.  <span data-ttu-id="99325-122">Se você não vir nenhum erro, tente acessar a seguinte URL a partir de qualquer outro computador na topologia:</span><span class="sxs-lookup"><span data-stu-id="99325-122">If you do not see any errors, try accessing the following URL from any other computer in the topology:</span></span>
    
    <span data-ttu-id="99325-123"> https:// \<fe-server\> /lRS</span><span class="sxs-lookup"><span data-stu-id="99325-123">https://\<fe-server\>/lrs</span></span>
    
    <span data-ttu-id="99325-124">Para acessar a página, você precisará adicionar os registros DNS conforme descrito em "registros de DNS necessários para a entrada automática do cliente" em [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056) .</span><span class="sxs-lookup"><span data-stu-id="99325-124">To access the page, you will need to add the DNS records as described in “Required DNS Records for Automatic Client Sign-In” at [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056).</span></span>

<span data-ttu-id="99325-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99325-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

