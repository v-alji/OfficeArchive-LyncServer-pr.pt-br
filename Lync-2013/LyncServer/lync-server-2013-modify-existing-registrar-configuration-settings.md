---
title: 'Lync Server 2013: modificar as definições de configuração de registradores existentes'
description: 'Lync Server 2013: modificar as configurações de registro existentes.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify existing Registrar configuration settings
ms:assetid: a8931511-3e66-49ed-a3ec-03bcd61ce1f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182566(v=OCS.15)
ms:contentKeyID: 48185095
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a4a58a73ec67a320a9d9ee9a29b8e0a4708aa40a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425476"
---
# <a name="modify-existing-registrar-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="f6dee-103">Modificar as definições de configuração do registrador existentes no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f6dee-103">Modify existing Registrar configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f6dee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f6dee-104">

<span> </span></span></span>

<span data-ttu-id="f6dee-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="f6dee-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="f6dee-106">Você pode usar o Registrador para configurar protocolos de autenticação de servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="f6dee-106">You can use the Registrar to configure proxy server authentication protocols.</span></span> <span data-ttu-id="f6dee-107">Para obter informações sobre os protocolos disponíveis, consulte [criar configurações de registrador de configuração no Lync Server 2013](lync-server-2013-create-registrar-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f6dee-107">For information about the available protocols, see [Create Registrar configuration settings in Lync Server 2013](lync-server-2013-create-registrar-configuration-settings.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f6dee-p102">Recomendamos a habilitação do Kerberos e NTLM quando um servidor suporta autenticação para clientes remotos e empresariais. O Servidor de Borda e os servidores internos se comunicam para assegurar que somente a autenticação NTLM seja oferecida aos clientes remotos. Se somente Kerberos for habilitado nesses servidores, não poderão autenticar usuários remotos. Se os usuários empresariais também autenticarem com base no servidor, o Kerberos será usado.</span><span class="sxs-lookup"><span data-stu-id="f6dee-p102">We recommend that you enable both Kerberos and NTLM when a server supports authentication for both remote and enterprise clients. The Edge Server and internal servers communicate to ensure that only NTLM authentication is offered to remote clients. If only Kerberos is enabled on these servers, they cannot authenticate remote users. If enterprise users also authenticate against the server, Kerberos is used.</span></span>



</div>

<span data-ttu-id="f6dee-112">Siga estas etapas para modificar um Registrador Avançado existente.</span><span class="sxs-lookup"><span data-stu-id="f6dee-112">Follow these steps to modify an existing Registrar.</span></span>

<div>

## <a name="to-modify-existing-registrar-configuration-settings"></a><span data-ttu-id="f6dee-113">Para modificar as configurações existentes do Registrador</span><span class="sxs-lookup"><span data-stu-id="f6dee-113">To modify existing registrar configuration settings</span></span>

1.  <span data-ttu-id="f6dee-114">Em uma conta de usuário que é membro do grupo RTCUniversalServerAdmins (ou tem direitos de usuário equivalentes) ou atribuído à função CsServerAdministrator ou CsAdministrator, faça logon em qualquer computador que esteja na rede na qual você implantou o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f6dee-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="f6dee-115">Abra uma janela do navegador e, em seguida, insira a URL de administração para abrir o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="f6dee-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f6dee-116">Para obter detalhes sobre os diferentes métodos que você pode usar para iniciar o painel de controle do Lync Server, consulte [abrir ferramentas administrativas do Lync server 2013](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f6dee-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f6dee-117">Na barra de navegação esquerda, clique em **Segurança** e em **Registrador**.</span><span class="sxs-lookup"><span data-stu-id="f6dee-117">In the left navigation bar, click **Security** and then click **Registrar**.</span></span>

4.  <span data-ttu-id="f6dee-118">Na página **Registrador Avançado**, clique em um serviço, em **Editar** e em **Exibir detalhes**.</span><span class="sxs-lookup"><span data-stu-id="f6dee-118">On the **Registrar** page, click a service, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="f6dee-119">Em **Editar Configuração do Registrador Avançado**, selecione um ou mais dos itens a seguir, dependendo dos recursos dos clientes e do suporte em seu ambiente:</span><span class="sxs-lookup"><span data-stu-id="f6dee-119">In **Edit Registrar Setting**, select one or more of the following depending on the capabilities of the clients and support in your environment:</span></span>
    
      - <span data-ttu-id="f6dee-120">**Habilitar autenticação Kerberos** para que os servidores no pool emitam desafios usando a autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="f6dee-120">**Enable Kerberos authentication** to have the servers in the pool issue challenges using Kerberos authentication.</span></span>
    
      - <span data-ttu-id="f6dee-121">**Habilitar autenticação NTLM** para que os servidores no pool emitam desafios usando NTLM.</span><span class="sxs-lookup"><span data-stu-id="f6dee-121">**Enable NTLM authentication** to have the servers in the pool issue challenges using NTLM.</span></span>
    
      - <span data-ttu-id="f6dee-122">**Habilitar autenticação de certificado** para que os servidores no pool emitam certificados para os clientes.</span><span class="sxs-lookup"><span data-stu-id="f6dee-122">**Enable certificate authentication** to have the servers in the pool issue certificates to clients.</span></span>

6.  <span data-ttu-id="f6dee-123">Clique em **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="f6dee-123">Click **Commit**.</span></span>

<span data-ttu-id="f6dee-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f6dee-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

