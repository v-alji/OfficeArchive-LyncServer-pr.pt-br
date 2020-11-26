---
title: 'Lync Server 2013: Instalando a Ferramenta de Planejamento'
description: 'Lync Server 2013: instalando a ferramenta de planejamento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Planning Tool
ms:assetid: ebdc9e26-4b22-4b02-85b9-7462bcfe7c93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615046(v=OCS.15)
ms:contentKeyID: 51541525
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 11836e2c86cb01d6f911670a9eeafef0c31c0af4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426904"
---
# <a name="installing-the-planning-tool-in-lync-server-2013"></a><span data-ttu-id="0fbeb-103">Instalando a Ferramenta de Planejamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0fbeb-103">Installing the Planning Tool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0fbeb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0fbeb-104">

<span> </span></span></span>

<span data-ttu-id="0fbeb-105">_**Tópico da última modificação:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="0fbeb-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="0fbeb-106">Antes de começar a criar e planejar a infraestrutura do Lync Server 2013 usando o Microsoft Lync Server 2013, ferramenta de planejamento, você deve primeiro instalar a ferramenta de planejamento.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-106">Before you begin designing and planning your Lync Server 2013 infrastructure by using the Microsoft Lync Server 2013, Planning Tool, you must first install the Planning Tool.</span></span> <span data-ttu-id="0fbeb-107">A ferramenta de planejamento não precisa ser implantada em uma estação de trabalho ou em um servidor que faça parte do domínio ou da infraestrutura em que você planeja instalar o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-107">The Planning Tool does not need to be deployed to a workstation or server that is part of the domain or infrastructure where you plan to install Lync Server 2013.</span></span> <span data-ttu-id="0fbeb-108">O arquivo Leiame que acompanha a ferramenta de planejamento detalha informações importantes sobre a instalação e a utilização da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-108">The Readme file that accompanies the Planning Tool details important information about installing and using the tool.</span></span> <span data-ttu-id="0fbeb-109">Algumas das informações no arquivo Leiame estão reproduzidas aqui para esclarecimento.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-109">Some of the information in the Readme file is duplicated here for clarity.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="0fbeb-110">A ferramenta de planejamento requer a instalação de um usuário com direitos e permissões de administrador no computador em que a ferramenta está instalada.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-110">The Planning Tool requires installation by a user with administrator rights and permissions on the computer on which the tool is to be installed.</span></span>



</div>

<span data-ttu-id="0fbeb-111">Os sistemas operacionais com suporte para instalação e operação da ferramenta de planejamento são:</span><span class="sxs-lookup"><span data-stu-id="0fbeb-111">The supported operating systems for installation and operation of the Planning Tool are:</span></span>

  - <span data-ttu-id="0fbeb-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0fbeb-112">Windows 8</span></span>

  - <span data-ttu-id="0fbeb-113">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0fbeb-113">Windows 8.1</span></span>

  - <span data-ttu-id="0fbeb-114">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0fbeb-114">Windows Server 2012</span></span>

  - <span data-ttu-id="0fbeb-115">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0fbeb-115">Windows Server 2012 R2</span></span>

  - <span data-ttu-id="0fbeb-116">Windows 7, edição de 32 bits</span><span class="sxs-lookup"><span data-stu-id="0fbeb-116">Windows 7, 32-bit edition</span></span>

  - <span data-ttu-id="0fbeb-117">Windows 7, edição de 64 bits usando Windows no Win32 (WOW)</span><span class="sxs-lookup"><span data-stu-id="0fbeb-117">Windows 7, 64-bit edition using Windows on Win32 (WOW)</span></span>

  - <span data-ttu-id="0fbeb-118">Windows Server 2008 R2, usando WOW</span><span class="sxs-lookup"><span data-stu-id="0fbeb-118">Windows Server 2008 R2, using WOW</span></span>

<span data-ttu-id="0fbeb-119">Além disso, a ferramenta de planejamento requer o Microsoft .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-119">Additionally, the Planning Tool requires Microsoft .NET Framework 4.5.</span></span>

<span data-ttu-id="0fbeb-120">Depois que os requisitos de pré-instalação forem atendidos, você poderá instalar a ferramenta de planejamento.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-120">After the preinstallation requirements are met, you can then install the Planning Tool.</span></span>

<div>

## <a name="to-install-the-planning-tool"></a><span data-ttu-id="0fbeb-121">Para instalar a Ferramenta de Planejamento</span><span class="sxs-lookup"><span data-stu-id="0fbeb-121">To install the Planning Tool</span></span>

1.  <span data-ttu-id="0fbeb-122">Faça logon no computador local como membro do grupo Administradores.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-122">Log on to the local computer as a member of the Administrators group.</span></span>

2.  <span data-ttu-id="0fbeb-123">Usando o Windows Explorer ou uma janela de comando, localize o diretório em que você baixou os arquivos de instalação da ferramenta de planejamento.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-123">Using Windows Explorer or a command window, locate the directory where you downloaded the Planning Tool installation files.</span></span>

3.  <span data-ttu-id="0fbeb-124">Localize o LyncPlanningTool.msi.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-124">Locate the LyncPlanningTool.msi.</span></span> <span data-ttu-id="0fbeb-125">No Windows Explorer, clique duas vezes no arquivo.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-125">In Windows Explorer, double-click the file.</span></span> <span data-ttu-id="0fbeb-126">Na janela de comando, digite o nome do arquivo e pressione  **Enter** para executá-lo.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-126">In the command window, type the name of the file, and then press **Enter** to run the file.</span></span>

4.  <span data-ttu-id="0fbeb-127">Na página de boas-vindas do **Microsoft Lync Server 2013, assistente de configuração da ferramenta de planejamento**, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-127">On the Welcome page of the **Microsoft Lync Server 2013, Planning Tool Setup Wizard**, click **Next**.</span></span>

5.  <span data-ttu-id="0fbeb-128">Revise o **Contrato de Licença de Usuário Final**, selecione **Aceito os termos do Contrato de Licença** se você escolher aceitar os termos de uso do contrato de licença e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-128">Review the **End-User License Agreement**, select **I accept the terms in the License Agreement** if you choose to accept the terms of use in the license agreement, and then click **Next**.</span></span>

6.  <span data-ttu-id="0fbeb-129">Escolha onde instalar os arquivos da ferramenta de planejamento.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-129">Choose where to install the Planning Tool files.</span></span> <span data-ttu-id="0fbeb-130">O local padrão é C: \\ arquivos de programas (x86) \\ Microsoft Lync Server 2013 \\ Planning Tool.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-130">The default location is C:\\Program Files (x86)\\Microsoft Lync Server 2013\\Planning Tool.</span></span> <span data-ttu-id="0fbeb-131">Se quiser alterar o local de instalação, clique em **Alterar**.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-131">If you want to change the installation location, click **Change**.</span></span> <span data-ttu-id="0fbeb-132">Em **Alterar pasta de destino**, procure ou digite o local para instalar os arquivos, clique em **OK** e, depois, em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-132">On **Change destination folder**, browse or type the location to install the files, click **OK**, and then click **Next**.</span></span>

7.  <span data-ttu-id="0fbeb-133">O instalador já está pronto para instalar a ferramenta de planejamento.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-133">The installer is now ready to install the Planning Tool.</span></span> <span data-ttu-id="0fbeb-134">Clique em **Instalar** para começar o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-134">Click **Install** to begin the installation process.</span></span>

8.  <span data-ttu-id="0fbeb-135">A instalação será iniciada e o andamento será exibido.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-135">The installation will start, and the progress will be displayed.</span></span> <span data-ttu-id="0fbeb-136">Após a conclusão da instalação, clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-136">After the installation is successfully completed, click **Finish**.</span></span>

9.  <span data-ttu-id="0fbeb-137">A ferramenta de planejamento está pronta para uso.</span><span class="sxs-lookup"><span data-stu-id="0fbeb-137">The Planning Tool is ready for use.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0fbeb-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fbeb-138">See Also</span></span>


[<span data-ttu-id="0fbeb-139">Instalação de software opcional no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0fbeb-139">Installing optional software in Lync Server 2013</span></span>](lync-server-2013-installing-optional-software.md)  
  

<span data-ttu-id="0fbeb-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0fbeb-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

