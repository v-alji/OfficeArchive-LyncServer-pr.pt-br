---
title: 'Lync Server 2013: Configurando o Diretor'
description: 'Lync Server 2013: Configurando o diretor.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up the Director
ms:assetid: 408b76f7-6fdd-4e50-8a3e-e87db12c1394
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425915(v=OCS.15)
ms:contentKeyID: 48183951
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2b917000dec6d30fdec2963ff1e464fbb9a70805
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423901"
---
# <a name="setting-up-the-director-in-lync-server-2013"></a><span data-ttu-id="d444a-103">Configurando o Diretor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d444a-103">Setting up the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d444a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d444a-104">

<span> </span></span></span>

<span data-ttu-id="d444a-105">_**Tópico da última modificação:** 2014-05-05_</span><span class="sxs-lookup"><span data-stu-id="d444a-105">_**Topic Last Modified:** 2014-05-05_</span></span>

<span data-ttu-id="d444a-106">Se você estiver habilitando o acesso para usuários externos implantando servidores de borda, uma opção é implantar um diretor.</span><span class="sxs-lookup"><span data-stu-id="d444a-106">If you’re enabling access for external users by deploying Edge Servers, one option is to deploy a Director.</span></span> <span data-ttu-id="d444a-107">Um diretor é um servidor que executa o Microsoft Lync Server 2013 que autentica solicitações do usuário, mas não hospeda nenhuma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="d444a-107">A Director is a server running Microsoft Lync Server 2013 that authenticates user requests, but doesn’t home any user accounts.</span></span> <span data-ttu-id="d444a-108">Isso não é um requisito, mas é muito útil se você estiver preocupado com o desempenho e quiser ajudar a simplificar as solicitações de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d444a-108">Now, this isn’t a requirement, but it is very helpful if you’re worried about performance and want to help streamline authentication requests.</span></span> <span data-ttu-id="d444a-109">Se você decidir que esta é uma boa ideia para a sua organização, as etapas para configurar um diretor ou um pool de directors são semelhantes a configurar um pool Front-end do Enterprise Edition ou um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d444a-109">If you decide this is a good idea for your organization, the steps to set up a Director or a Director pool are similar to setting up either an Enterprise Edition Front End pool or Standard Edition server.</span></span> <span data-ttu-id="d444a-110">Depois de definir seu (s) Diretor (s) no construtor de topologias, você precisará executar as etapas desta seção.</span><span class="sxs-lookup"><span data-stu-id="d444a-110">After you’ve defined your Director(s) in Topology Builder, you’ll need to perform the steps in this section.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d444a-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d444a-111">In This Section</span></span>

  - [<span data-ttu-id="d444a-112">Instalar o repositório de Configuração Local no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d444a-112">Install the Local Configuration store in Lync Server 2013</span></span>](lync-server-2013-install-the-local-configuration-store.md)

  - [<span data-ttu-id="d444a-113">Instalar o Lync Server 2013 no Diretor</span><span class="sxs-lookup"><span data-stu-id="d444a-113">Install Lync Server 2013 on the Director</span></span>](lync-server-2013-install-lync-server-on-the-director.md)

  - [<span data-ttu-id="d444a-114">Configurar certificados do Diretor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d444a-114">Configure certificates for the Director in Lync Server 2013</span></span>](lync-server-2013-configure-certificates-for-the-director.md)

  - [<span data-ttu-id="d444a-115">Iniciar os serviços no diretor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d444a-115">Start services on the Director in Lync Server 2013</span></span>](lync-server-2013-start-services-on-the-director.md)

  - [<span data-ttu-id="d444a-116">Testar o Diretor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d444a-116">Test the Director in Lync Server 2013</span></span>](lync-server-2013-test-the-director.md)

  - [<span data-ttu-id="d444a-117">Configurar Entrada Automática de Cliente para usar o Diretor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d444a-117">Configure Automatic Client Sign-In to use the Director in Lync Server 2013</span></span>](lync-server-2013-configure-automatic-client-sign-in-to-use-the-director.md)

<span data-ttu-id="d444a-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d444a-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

