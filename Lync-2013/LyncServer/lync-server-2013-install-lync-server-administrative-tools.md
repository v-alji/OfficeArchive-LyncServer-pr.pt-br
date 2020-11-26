---
title: 'Lync Server 2013: Instalar ferramentas administrativas do Lync Server'
description: 'Lync Server 2013: instalar as ferramentas administrativas do Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Lync Server administrative tools
ms:assetid: 842b85e4-2eeb-464f-b1c1-ceb8cc04f8d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398665(v=OCS.15)
ms:contentKeyID: 48184695
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ca1ad96299197c3339d06c4f094784edc632e6b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427191"
---
# <a name="install-lync-server-2013-administrative-tools"></a><span data-ttu-id="495ad-103">Instalar ferramentas administrativas do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="495ad-103">Install Lync Server 2013 administrative tools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="495ad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="495ad-104">

<span> </span></span></span>

<span data-ttu-id="495ad-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="495ad-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="495ad-106">Este tópico descreve como instalar as ferramentas administrativas que você precisa usar para implantar e gerenciar o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="495ad-106">This topic describes how to install the administrative tools you need to use to deploy and manage Lync Server 2013.</span></span> <span data-ttu-id="495ad-107">As ferramentas administrativas são instaladas por padrão em cada servidor que executa o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="495ad-107">The administrative tools are installed by default on each server running Lync Server 2013.</span></span> <span data-ttu-id="495ad-108">Além disso, você pode instalar as ferramentas administrativas em outros computadores, como consoles administrativos dedicados.</span><span class="sxs-lookup"><span data-stu-id="495ad-108">Additionally, you can install the administrative tools on other computers, such as dedicated administrative consoles.</span></span> <span data-ttu-id="495ad-109">É altamente recomendável que você instale as ferramentas administrativas em um computador que esteja no mesmo domínio ou floresta que a implantação do Lync Server 2013 que você está criando porque está fazendo isso, verifique se as etapas de preparação dos serviços de domínio Active Directory já foram concluídas, o que permite que você use as ferramentas administrativas nesse computador posteriormente para publicar sua topologia.</span><span class="sxs-lookup"><span data-stu-id="495ad-109">We strongly recommend that you install the administrative tools on a computer that is in the same domain or forest as the Lync Server 2013 deployment you are creating because by doing so you make sure that Active Directory Domain Services preparation steps are already complete, which enables you to use the administrative tools on that computer later to publish your topology.</span></span>

<span data-ttu-id="495ad-110">Verifique se revisar os requisitos de infraestrutura, sistema operacional, software e administrador antes de instalar ou usar as ferramentas administrativas do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="495ad-110">Make sure that you review infrastructure, operating system, software, and administrator rights requirements before you install or use the Lync Server 2013 administrative tools.</span></span> <span data-ttu-id="495ad-111">Para obter detalhes sobre requisitos de infraestrutura, consulte [requisitos de infraestrutura de ferramentas administrativas no Lync Server 2013](lync-server-2013-administrative-tools-infrastructure-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="495ad-111">For details about infrastructure requirements, see [Administrative tools infrastructure requirements in Lync Server 2013](lync-server-2013-administrative-tools-infrastructure-requirements.md).</span></span> <span data-ttu-id="495ad-112">Para obter detalhes sobre os requisitos do sistema operacional e do software para instalar as ferramentas administrativas do Lync Server 2013, consulte [suporte ao sistema operacional do servidor e ferramentas no Lync server 2013](lync-server-2013-server-and-tools-operating-system-support.md), [requisitos de software adicionais para o Lync Server 2013](lync-server-2013-additional-software-requirements.md), além [de requisitos e suporte de servidor adicionais no Lync Server 2013](lync-server-2013-additional-server-support-and-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="495ad-112">For details about operating system and software requirements to install the Lync Server 2013 administrative tools, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md), [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md), and [Additional server support and requirements in Lync Server 2013](lync-server-2013-additional-server-support-and-requirements.md).</span></span> <span data-ttu-id="495ad-113">Para obter detalhes sobre os direitos de usuário e as permissões necessárias para instalar e usar as ferramentas, consulte [direitos de administrador e permissões necessárias para a instalação e a administração do Lync Server 2013](lync-server-2013-administrator-rights-and-permissions-required-for-setup-and-administration.md).</span><span class="sxs-lookup"><span data-stu-id="495ad-113">For details about the user rights and permissions required to install and use the tools, see [Administrator rights and permissions required for setup and administration of Lync Server 2013](lync-server-2013-administrator-rights-and-permissions-required-for-setup-and-administration.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="495ad-114">Se a sua organização exigir que você localize os serviços de informações da Internet (IIS) e todos os serviços Web em uma unidade diferente da unidade do sistema, você poderá alterar o caminho do local de instalação dos arquivos do Lync Server na caixa de diálogo Configurar.</span><span class="sxs-lookup"><span data-stu-id="495ad-114">If your organization requires that you locate Internet Information Services (IIS) and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server files in the Setup dialog box.</span></span> <span data-ttu-id="495ad-115">Se você instalar os arquivos de instalação nesse caminho, incluindo OCSCore.msi, o restante dos arquivos do Lync Server 2013 também será implantado nessa unidade.</span><span class="sxs-lookup"><span data-stu-id="495ad-115">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will be deployed to this drive as well.</span></span>



</div>

<div>

## <a name="to-install-the-lync-server-2013-administrative-tools"></a><span data-ttu-id="495ad-116">Para instalar as ferramentas administrativas do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="495ad-116">To install the Lync Server 2013 administrative tools</span></span>

1.  <span data-ttu-id="495ad-117">Faça logon como administrador local (requisito mínimo) para o computador em que você deseja instalar as ferramentas administrativas.</span><span class="sxs-lookup"><span data-stu-id="495ad-117">Log on as a local administrator (minimum requirement) to the computer where you want to install the administrative tools.</span></span> <span data-ttu-id="495ad-118">Se você estiver conectado como um usuário padrão nos sistemas operacionais Windows Vista ou Windows 7, e o controle de conta de usuário (UAC) estiver habilitado, você será solicitado a fornecer o administrador local ou um nome de usuário e uma senha equivalentes ao domínio.</span><span class="sxs-lookup"><span data-stu-id="495ad-118">If you are logged on as an a standard user on the Windows Vista or Windows 7 operating systems, and User Account Control (UAC) is enabled, you will be prompted for the local administrator or a domain equivalent user name and password.</span></span>

2.  <span data-ttu-id="495ad-119">Localize a mídia de instalação no seu computador e, em seguida, clique duas vezes em \\ Setup \\ AMD64 \\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="495ad-119">Locate the installation media on your computer, and then double-click \\Setup\\amd64\\Setup.exe.</span></span>

3.  <span data-ttu-id="495ad-120">Se você for solicitado a instalar o Microsoft Visual C++ 2008 Redistributable, clique em **Sim**.</span><span class="sxs-lookup"><span data-stu-id="495ad-120">If you are prompted to install the Microsoft Visual C++ 2008 distributable, click **Yes**.</span></span>

4.  <span data-ttu-id="495ad-121">Na página **local de instalação do Microsoft Lync Server 2013** , clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="495ad-121">On the **Microsoft Lync Server 2013 Installation Location** page, click **OK**.</span></span> <span data-ttu-id="495ad-122">Altere esse caminho para outro local ou unidade se precisar ter os arquivos instalados em outro local.</span><span class="sxs-lookup"><span data-stu-id="495ad-122">Change this path to another location or drive if you need to have the files installed to another location.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="495ad-123">Se a sua organização exigir que você localize os serviços de informações da Internet (IIS) e todos os serviços Web em uma unidade diferente da unidade do sistema, você poderá alterar o caminho do local de instalação dos arquivos do Lync Server 2013 na caixa de diálogo Configurar.</span><span class="sxs-lookup"><span data-stu-id="495ad-123">If your organization requires that you locate Internet Information Services (IIS) and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server 2013 files in the Setup dialog box.</span></span> <span data-ttu-id="495ad-124">Se você instalar os arquivos de instalação nesse caminho, incluindo OCSCore.msi, o restante dos arquivos do Lync Server 2013 será implantado nesta unidade também.</span><span class="sxs-lookup"><span data-stu-id="495ad-124">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will be deployed to this drive too.</span></span>

    
    </div>

5.  <span data-ttu-id="495ad-125">Na página **contrato de licença de usuário final** , examine os termos de licença, clique em **aceito** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="495ad-125">On the **End User License Agreement** page, review the license terms, click **I accept**, and then click **OK**.</span></span> <span data-ttu-id="495ad-126">Esta etapa é necessária para que você possa continuar.</span><span class="sxs-lookup"><span data-stu-id="495ad-126">This step is required before you can continue.</span></span>

6.  <span data-ttu-id="495ad-127">Na página **Microsoft Lync Server 2013 – assistente de implantação** , clique em **instalar ferramentas de administrador**.</span><span class="sxs-lookup"><span data-stu-id="495ad-127">On the **Microsoft Lync Server 2013 – Deployment Wizard** page, click **Install Administrator Tools**.</span></span>

7.  <span data-ttu-id="495ad-128">Quando a instalação for concluída com êxito, clique em **sair**.</span><span class="sxs-lookup"><span data-stu-id="495ad-128">When the installation successfully completes, click **Exit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="495ad-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="495ad-129">See Also</span></span>


[<span data-ttu-id="495ad-130">Abrir ferramentas administrativas do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="495ad-130">Open Lync Server 2013 administrative tools</span></span>](lync-server-2013-open-lync-server-administrative-tools.md)  


[<span data-ttu-id="495ad-131">Ferramentas administrativas do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="495ad-131">Lync Server 2013 administrative tools</span></span>](lync-server-2013-lync-server-administrative-tools.md)  
  

<span data-ttu-id="495ad-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="495ad-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

