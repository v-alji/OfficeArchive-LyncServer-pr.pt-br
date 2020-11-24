---
title: 'Lync Server 2013: Ferramentas de gerenciamento do Windows PowerShell e do Lync Server'
description: 'Lync Server 2013: ferramentas de gerenciamento do Windows PowerShell e do Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Windows PowerShell and Lync Server 2013 management tools
ms:assetid: 6a285f7c-0ef5-4cab-9976-d03be276e35d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481130(v=OCS.15)
ms:contentKeyID: 59893869
ms.date: 07/20/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11c8d63974ad05a041eb446182cbc7f9336044b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390023"
---
# <a name="windows-powershell-and-lync-server-2013-management-tools"></a><span data-ttu-id="f3158-103">Ferramentas de gerenciamento do Windows PowerShell e do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3158-103">Windows PowerShell and Lync Server 2013 management tools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3158-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3158-104">

<span> </span></span></span>

<span data-ttu-id="f3158-105">_**Tópico da última modificação:** 2016-07-20_</span><span class="sxs-lookup"><span data-stu-id="f3158-105">_**Topic Last Modified:** 2016-07-20_</span></span>

<span data-ttu-id="f3158-106">No Microsoft Lync Server 2013, as ferramentas de gerenciamento são implementadas usando o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3158-106">In Microsoft Lync Server 2013, management tools are implemented using Windows PowerShell.</span></span> <span data-ttu-id="f3158-107">O Windows PowerShell inclui um ambiente de linha de comando, comandos específicos do produto e uma linguagem de script completa.</span><span class="sxs-lookup"><span data-stu-id="f3158-107">Windows PowerShell includes a command-line environment, product-specific commands, and a full scripting language.</span></span> <span data-ttu-id="f3158-108">As ferramentas do Lync Server 2013 implementadas usando o Windows PowerShell incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f3158-108">Lync Server 2013 tools that are implemented using Windows PowerShell include the following:</span></span>

  - <span data-ttu-id="f3158-109">**Construtor de topologias**.</span><span class="sxs-lookup"><span data-stu-id="f3158-109">**Topology Builder**.</span></span> <span data-ttu-id="f3158-110">Você usa o construtor de topologias para criar, ajustar e publicar sua topologia planejada e valida sua topologia antes de iniciar instalações de servidor.</span><span class="sxs-lookup"><span data-stu-id="f3158-110">You use Topology Builder to create, adjust, and publish your planned topology, and it validates your topology before you begin server installations.</span></span> <span data-ttu-id="f3158-111">Quando você instala o Lync Server 2013 em servidores individuais, os servidores lêem a topologia publicada como parte do processo de instalação, e o programa de instalação implanta o servidor conforme direcionado na topologia.</span><span class="sxs-lookup"><span data-stu-id="f3158-111">When you install Lync Server 2013 on individual servers, the servers read the published topology as part of the installation process, and the installation program deploys the server as directed in the topology.</span></span> <span data-ttu-id="f3158-112">After setup, configuration information is automatically replicated to all servers.</span><span class="sxs-lookup"><span data-stu-id="f3158-112">After setup, configuration information is automatically replicated to all servers.</span></span> <span data-ttu-id="f3158-113">Components can be added to your deployment only by using Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="f3158-113">Components can be added to your deployment only by using Topology Builder.</span></span>

  - <span data-ttu-id="f3158-114">**Shell de gerenciamento do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="f3158-114">**Lync Server Management Shell**.</span></span> <span data-ttu-id="f3158-115">Você pode usar o Shell de gerenciamento do Lync Server para o gerenciamento de linha de comando completo da sua implantação.</span><span class="sxs-lookup"><span data-stu-id="f3158-115">You can use Lync Server Management Shell for full command-line management of your deployment.</span></span>

  - <span data-ttu-id="f3158-116">**Painel de controle do Lync Server**.</span><span class="sxs-lookup"><span data-stu-id="f3158-116">**Lync Server Control Panel**.</span></span> <span data-ttu-id="f3158-117">Você pode usar a interface do usuário do painel de controle do Microsoft Lync Server 2013 para gerenciar as tarefas mais comuns na sua implantação.</span><span class="sxs-lookup"><span data-stu-id="f3158-117">You can use the Microsoft Lync Server 2013 Control Panel user interface to manage the most common tasks in your deployment.</span></span>

<span data-ttu-id="f3158-118">Essas ferramentas usam cmdlets do Windows PowerShell para o gerenciamento da sua implantação, incluindo cmdlets próximos a 550 cmdlets específicos do produto.</span><span class="sxs-lookup"><span data-stu-id="f3158-118">These tools use Windows PowerShell cmdlets for management of your deployment, including close to 550 product-specific cmdlets.</span></span> <span data-ttu-id="f3158-119">Os cmdlets de segurança incluídos no Lync Server 2013 são usados principalmente para gerenciar autenticação e direitos e permissões de usuário.</span><span class="sxs-lookup"><span data-stu-id="f3158-119">The security cmdlets included in Lync Server 2013 are primarily used to manage authentication, and user rights and permissions.</span></span> <span data-ttu-id="f3158-120">Uma ampla variedade de cmdlets está disponível para o gerenciamento da autenticação, incluindo cmdlets para autenticação de certificado e de PIN (número de identificação pessoal).</span><span class="sxs-lookup"><span data-stu-id="f3158-120">A wide variety of cmdlets are available for managing authentication, including cmdlets for certificate and personal identification number (PIN) authentication.</span></span> <span data-ttu-id="f3158-121">Além disso, vários cmdlets permitem que você use o novo recurso de controle de acesso à Role-Based (RBAC) para delegar o controle administrativo do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f3158-121">In addition, a number of cmdlets enable you to use the new Role-Based Access Control (RBAC) feature to delegate administrative control of Lync Server 2013.</span></span> <span data-ttu-id="f3158-122">Para obter detalhes sobre os cmdlets do Lync Server, consulte [Shell de gerenciamento do Lync server 2013](lync-server-2013-lync-server-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="f3158-122">For details about the Lync Server cmdlets, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span></span>

<span data-ttu-id="f3158-123">Os recursos de segurança de script para Windows PowerShell foram projetados especificamente para ajudar a prevenir alguns problemas de segurança relacionados a scripts de tecnologias mais antigas, incluindo o Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="f3158-123">The script security features for Windows PowerShell are specifically designed to help prevent some of the scripting-related security problems of older technologies, including Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="f3158-124">Os recursos de segurança do Windows PowerShell destinam-se a criar um ambiente no qual os usuários não podem executar scripts de forma fácil ou desconhecida.</span><span class="sxs-lookup"><span data-stu-id="f3158-124">The Windows PowerShell security features are intended to create an environment in which users cannot easily or unknowingly run scripts.</span></span> <span data-ttu-id="f3158-125">Por padrão, os recursos de segurança do Windows PowerShell estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="f3158-125">By default, Windows PowerShell security features are enabled.</span></span> <span data-ttu-id="f3158-126">Você pode modificar o estado desses recursos para atender às suas necessidades de script e cumprir vários objetivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="f3158-126">You can modify the state of those features to accommodate your scripting needs and a variety of security goals.</span></span> <span data-ttu-id="f3158-127">Isso não quer dizer que o shell impossibilite os usuários de executar scripts.</span><span class="sxs-lookup"><span data-stu-id="f3158-127">This is not to say that the shell makes it impossible for users to run scripts.</span></span> <span data-ttu-id="f3158-128">Em vez disso, o shell dificulta, por padrão, que os usuários executem scripts sem perceber.</span><span class="sxs-lookup"><span data-stu-id="f3158-128">Rather, the shell makes it difficult—by default—for users to run scripts without realizing they are doing so.</span></span> <span data-ttu-id="f3158-129">Para obter detalhes, consulte segurança de script do Windows PowerShell em [https://go.microsoft.com/fwlink/p/?LinkId=213145](https://go.microsoft.com/fwlink/p/?linkid=213145) .</span><span class="sxs-lookup"><span data-stu-id="f3158-129">For details, see Windows PowerShell Script Security at [https://go.microsoft.com/fwlink/p/?LinkId=213145](https://go.microsoft.com/fwlink/p/?linkid=213145).</span></span>

<span data-ttu-id="f3158-130"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3158-130"></div>

<span> </span>

</div>

</div>

</span></span></div>

