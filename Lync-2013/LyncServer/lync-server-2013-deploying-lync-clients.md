---
title: 'Lync Server 2013: Implantando clientes do Lync'
description: 'Lync Server 2013: Implantando clientes do Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync clients
ms:assetid: 3d10abf2-d484-4fa0-8f10-4a5f9dfba4f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204827(v=OCS.15)
ms:contentKeyID: 48183925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 09b501fc721ac880c5cf7da0293e3aa9c6443722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429983"
---
# <a name="deploying-lync-clients-in-lync-server-2013"></a><span data-ttu-id="57272-103">Implantando clientes do Lync no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57272-103">Deploying Lync clients in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="57272-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="57272-104">

<span> </span></span></span>

<span data-ttu-id="57272-105">_**Tópico da última modificação:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="57272-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="57272-106">O Lync 2013 introduz uma abordagem diferente para a implantação do cliente.</span><span class="sxs-lookup"><span data-stu-id="57272-106">Lync 2013 introduces a different approach to client deployment.</span></span> <span data-ttu-id="57272-107">Em uma partida de versões anteriores, o Lync 2013 não tem mais seu próprio instalador.</span><span class="sxs-lookup"><span data-stu-id="57272-107">In a departure from previous releases, Lync 2013 no longer has its own installer.</span></span> <span data-ttu-id="57272-108">Em vez disso, o Lync está incluído no programa de instalação do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="57272-108">Instead, Lync is included with the Office 2013 setup program.</span></span> <span data-ttu-id="57272-109">Para implantar o Lync 2013 em seus usuários, você pode usar os métodos de instalação e ferramentas de personalização do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="57272-109">To deploy Lync 2013 to your users, you can use Office 2013 installation methods and customization tools.</span></span>

  - <span data-ttu-id="57272-110">**Office 2013 o Windows Installer** é um pacote de instalação baseado no Windows Installer que consiste em vários arquivos MSI.</span><span class="sxs-lookup"><span data-stu-id="57272-110">**Office 2013 Windows Installer** is a Windows Installer-based installation package that consists of multiple MSI files.</span></span> <span data-ttu-id="57272-111">Um pacote de núcleo MSI de linguagem neutra é combinado com um ou mais pacotes de linguagem específica para fazer um produto completo.</span><span class="sxs-lookup"><span data-stu-id="57272-111">A language-neutral core MSI package is combined with one or more language-specific packages to make a complete product.</span></span> <span data-ttu-id="57272-112">A instalação reúne os pacotes individuais e efetua a personalização e tarefas de manutenção durante e após a instalação do Office nos computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="57272-112">Setup assembles the individual packages and performs customization and maintenance tasks during and after installation of Office on users' computers.</span></span> <span data-ttu-id="57272-113">Os tópicos desta seção descrevem como usar e personalizar o instalador do Windows do Office 2013 para implantar o Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="57272-113">The topics in this section describe how to use and customize the Office 2013 Windows Installer to deploy Lync 2013.</span></span>

  - <span data-ttu-id="57272-114">O **Office 2013 clique para executar** é um programa de instalação que transmite os arquivos de instalação do Office para o usuário do centro de administração do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="57272-114">**Office 2013 Click-to-Run** is an installation program that streams Office setup files to the user from the Microsoft 365 admin center.</span></span> <span data-ttu-id="57272-115">Os administradores podem personalizar a instalação utilizando a Ferramenta de Implantação do Office para Clique para Executar.</span><span class="sxs-lookup"><span data-stu-id="57272-115">Administrators can customize installation by using the Office Deployment Tool for Click-to-Run.</span></span> <span data-ttu-id="57272-116">Como o Office 2013 com Clique para executar é usado principalmente no ambiente do Microsoft 365, este método de instalação não está descrito em detalhes nesta seção.</span><span class="sxs-lookup"><span data-stu-id="57272-116">Because Office 2013 Click-to-Run is primarily used in the Microsoft 365 environment, this installation method is not described in detail in this section.</span></span> <span data-ttu-id="57272-117">Informações detalhadas sobre como usar e personalizar a instalação do clique para executar estão disponíveis na documentação do Office 2013 Resource Kit.</span><span class="sxs-lookup"><span data-stu-id="57272-117">Detailed information about using and customizing Click-to-Run installation is available in the Office 2013 Resource Kit documentation.</span></span> <span data-ttu-id="57272-118">Os administradores também podem baixar os arquivos de código-fonte do Office 2013 e os arquivos de idioma do Office para um local local, o que é útil quando você deseja minimizar a demanda na rede ou impedir que os usuários instalem o software da Internet por causa dos requisitos de segurança da empresa.</span><span class="sxs-lookup"><span data-stu-id="57272-118">Administrators can also download the Office 2013 Click-to-Run program and language source files to an on-premises location, which is useful when you want to minimize the demand on the network or prevent users from installing software from the Internet because of corporate security requirements.</span></span>

<span data-ttu-id="57272-119">Os tópicos desta seção se concentram em como implantar clientes usando o instalador baseado em MSI do Office 2013.</span><span class="sxs-lookup"><span data-stu-id="57272-119">The topics in this section focus on how to deploy clients by using the Office 2013 MSI-based installer.</span></span> <span data-ttu-id="57272-120">Sua referência principal deve ser a documentação do Office 2013 Resource Kit, que descreve em detalhes como preparar sua infraestrutura, personalizar a instalação e implantar o Office 2013.</span><span class="sxs-lookup"><span data-stu-id="57272-120">Your primary reference should be the Office 2013 Resource Kit documentation, which describes in detail how to prepare your infrastructure, customize setup, and deploy Office 2013.</span></span> <span data-ttu-id="57272-121">No entanto, você deve usar a documentação do Office em conjunto com os tópicos desta seção, que apontam as considerações de implantação específicas do Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="57272-121">However, you should use the Office documentation in conjunction with topics in this section, which point out deployment considerations that are specific to Lync 2013.</span></span>

<div>


> [!NOTE]  
> <UL>
> <LI>
> <P><span data-ttu-id="57272-122">O suplemento de reunião online do Lync 2013, que dá suporte ao gerenciamento de reuniões dentro do cliente de mensagens e colaboração do Outlook, é instalado automaticamente com o Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="57272-122">The Online Meeting Add-in for Lync 2013, which supports meeting management from within the Outlook messaging and collaboration client, installs automatically with Lync 2013.</span></span></P>
> <LI>
> <P><span data-ttu-id="57272-123">O programa de instalação do Office 2013 não desinstala versões anteriores do Lync ou do Office Communicator.</span><span class="sxs-lookup"><span data-stu-id="57272-123">The Office 2013 setup program does not uninstall previous versions of Lync or Office Communicator.</span></span> <span data-ttu-id="57272-124">O cliente do Lync 2013 é instalado lado a lado com outros clientes do Lync ou do Office Communicator</span><span class="sxs-lookup"><span data-stu-id="57272-124">The Lync 2013 client installs side-by-side with other Lync or Office Communicator clients</span></span></P></LI></UL>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="57272-125">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="57272-125">In This Section</span></span>

  - [<span data-ttu-id="57272-126">Personalizando a instalação do cliente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57272-126">Customizing client installation in Lync Server 2013</span></span>](lync-server-2013-customizing-client-installation.md)

  - [<span data-ttu-id="57272-127">Personalizando o comportamento do Lync e a interface do usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57272-127">Customizing Lync behavior and the user interface in Lync Server 2013</span></span>](lync-server-2013-customizing-lync-behavior-and-the-user-interface.md)

  - [<span data-ttu-id="57272-128">Personalizando o suplemento de reunião online no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57272-128">Customizing the Online Meeting Add-in in Lync Server 2013</span></span>](lync-server-2013-customizing-the-online-meeting-add-in.md)

  - [<span data-ttu-id="57272-129">Configurando a página de ingresso na reunião no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57272-129">Configuring the meeting join page in Lync Server 2013</span></span>](lync-server-2013-configuring-the-meeting-join-page.md)

  - [<span data-ttu-id="57272-130">Configurando as versões de cliente com suporte no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57272-130">Configuring supported client versions in Lync Server 2013</span></span>](lync-server-2013-configuring-supported-client-versions.md)

  - [<span data-ttu-id="57272-131">Configurando o modo de privacidade de presença avançada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57272-131">Configuring enhanced presence privacy mode in Lync Server 2013</span></span>](lync-server-2013-configuring-enhanced-presence-privacy-mode.md)

<span data-ttu-id="57272-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="57272-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

