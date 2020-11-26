---
title: 'Lync Server 2013: preparando e instalando o analisador de práticas recomendadas'
description: 'Lync Server 2013: preparando e instalando o analisador de práticas recomendadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing for and installing Best Practices Analyzer
ms:assetid: 550613dd-dc08-482e-9980-a3fe187cd162
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591347(v=OCS.15)
ms:contentKeyID: 48184149
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 005c5ac372a3564e74af549832830ebae899e9d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424139"
---
# <a name="preparing-for-and-installing-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="91ea8-103">Preparando e instalando o analisador de práticas recomendadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91ea8-103">Preparing for and installing Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91ea8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91ea8-104">

<span> </span></span></span>

<span data-ttu-id="91ea8-105">_**Tópico da última modificação:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="91ea8-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="91ea8-106">Você deve estar conectado como um membro do grupo Administradores para executar as tarefas descritas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="91ea8-106">You must be logged on as a member of the Administrators group to perform the tasks that are described in this topic.</span></span>

<div>

## <a name="system-requirements-for-best-practices-analyzer-installation"></a><span data-ttu-id="91ea8-107">Requisitos do sistema para a instalação do analisador de práticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="91ea8-107">System Requirements for Best Practices Analyzer Installation</span></span>

<span data-ttu-id="91ea8-108">Para executar o Lync Server 2013, o analisador de práticas recomendadas para verificar seu ambiente, o computador deve estar executando uma edição de 64 bits de um dos seguintes sistemas operacionais:</span><span class="sxs-lookup"><span data-stu-id="91ea8-108">To run Lync Server 2013, Best Practices Analyzer to scan your environment, the computer must be running a 64-bit edition of one of the following operating systems:</span></span>

  - <span data-ttu-id="91ea8-109">Sistema operacional padrão do Windows Server 2008 R2 com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="91ea8-109">Windows Server 2008 R2 with Service Pack 1 (SP1) Standard operating system</span></span>

  - <span data-ttu-id="91ea8-110">Sistema operacional Windows Server 2008 R2 com SP1 Enterprise</span><span class="sxs-lookup"><span data-stu-id="91ea8-110">Windows Server 2008 R2 with SP1 Enterprise operating system</span></span>

  - <span data-ttu-id="91ea8-111">Sistema operacional de datacenter do Windows Server 2008 R2 com SP1</span><span class="sxs-lookup"><span data-stu-id="91ea8-111">Windows Server 2008 R2 with SP1 Datacenter operating system</span></span>

  - <span data-ttu-id="91ea8-112">Sistema operacional Windows Server 2012 datacenter</span><span class="sxs-lookup"><span data-stu-id="91ea8-112">Windows Server 2012 Datacenter operating system</span></span>

  - <span data-ttu-id="91ea8-113">Sistema operacional padrão do Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91ea8-113">Windows Server 2012 Standard operating system</span></span>

  - <span data-ttu-id="91ea8-114">Sistema operacional Windows Server 2012 Enterprise</span><span class="sxs-lookup"><span data-stu-id="91ea8-114">Windows Server 2012 Enterprise operating system</span></span>

  - <span data-ttu-id="91ea8-115">Sistema operacional Windows Server 2012 R2 Datacenter</span><span class="sxs-lookup"><span data-stu-id="91ea8-115">Windows Server 2012 R2 Datacenter operating system</span></span>

  - <span data-ttu-id="91ea8-116">Sistema operacional padrão do Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="91ea8-116">Windows Server 2012 R2 Standard operating system</span></span>

  - <span data-ttu-id="91ea8-117">Sistema operacional Windows Server 2012 R2 Enterprise</span><span class="sxs-lookup"><span data-stu-id="91ea8-117">Windows Server 2012 R2 Enterprise operating system</span></span>

  - <span data-ttu-id="91ea8-118">Sistema operacional Windows 8</span><span class="sxs-lookup"><span data-stu-id="91ea8-118">Windows 8 operating system</span></span>

  - <span data-ttu-id="91ea8-119">Sistema operacional Windows 7</span><span class="sxs-lookup"><span data-stu-id="91ea8-119">Windows 7 operating system</span></span>

<span data-ttu-id="91ea8-120">O computador também deve estar executando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="91ea8-120">The computer must also be running the following:</span></span>

  - <span data-ttu-id="91ea8-121">Microsoft .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="91ea8-121">Microsoft .NET Framework 4.5.</span></span> <span data-ttu-id="91ea8-122">Para o Lync Server 2013, você deve instalar manualmente a edição de 64 bits do Microsoft .NET Framework 4,5 no servidor antes de instalar o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="91ea8-122">For Lync Server 2013, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span>

  - <span data-ttu-id="91ea8-123">Lync Server 2013, componentes principais.</span><span class="sxs-lookup"><span data-stu-id="91ea8-123">Lync Server 2013, Core Components.</span></span>

  - <span data-ttu-id="91ea8-124">Pacote de compatibilidade com versões anteriores do WMI.</span><span class="sxs-lookup"><span data-stu-id="91ea8-124">WMI Backward Compatibility Package.</span></span> <span data-ttu-id="91ea8-125">Para obter detalhes, consulte [instalar o pacote de compatibilidade com versões anteriores do WMI](install-wmi-backward-compatibility-package.md) na documentação de migração.</span><span class="sxs-lookup"><span data-stu-id="91ea8-125">For details, see [Install WMI Backward Compatibility package](install-wmi-backward-compatibility-package.md) in the Migration documentation.</span></span>

  - <span data-ttu-id="91ea8-126">Windows PowerShell 3,0.</span><span class="sxs-lookup"><span data-stu-id="91ea8-126">Windows PowerShell 3.0.</span></span> <span data-ttu-id="91ea8-127">Para obter detalhes, consulte [instalando o Windows PowerShell 3,0 para Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md) na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="91ea8-127">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md) in the Deployment documentation.</span></span>

<span data-ttu-id="91ea8-128">Você pode instalar o analisador de práticas recomendadas em computadores com um sistema operacional com suporte que não esteja executando o Lync Server 2013, componentes principais ou pacote de compatibilidade com versões anteriores do WMI, mas você pode usar o analisador de práticas recomendadas somente nesses computadores para ver relatórios, não para executar verificações.</span><span class="sxs-lookup"><span data-stu-id="91ea8-128">You can install Best Practices Analyzer on computers with a supported operating system that are not running Lync Server 2013, Core Components or WMI Backward Compatibility Package, but you can use Best Practices Analyzer on those computers only to view reports, not to run scans.</span></span>

</div>

<div>

## <a name="choosing-a-computer-for-installation"></a><span data-ttu-id="91ea8-129">Escolher um computador para instalação</span><span class="sxs-lookup"><span data-stu-id="91ea8-129">Choosing a Computer for Installation</span></span>

<span data-ttu-id="91ea8-130">Recomendamos que você instale o Lync Server 2013, o analisador de práticas recomendadas em um computador dedicado ao gerenciamento do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="91ea8-130">We recommend that you install Lync Server 2013, Best Practices Analyzer on a computer that is dedicated to Lync Server 2013 management.</span></span> <span data-ttu-id="91ea8-131">Você pode instalar a ferramenta em um servidor que executa o Lync Server 2013 ou um computador administrativo executando o Lync Server 2013 ferramentas administrativas.</span><span class="sxs-lookup"><span data-stu-id="91ea8-131">You can install the tool on a server running Lync Server 2013 or an administrative computer running Lync Server 2013 administrative tools.</span></span> <span data-ttu-id="91ea8-132">Se você instalar a ferramenta em um servidor que está executando o Lync Server, recomendamos usar a ferramenta para verificar somente esse servidor.</span><span class="sxs-lookup"><span data-stu-id="91ea8-132">If you install the tool on a server that is running Lync Server, we recommend that you use the tool to scan only that server.</span></span>

</div>

<div>

## <a name="installing-best-practices-analyzer"></a><span data-ttu-id="91ea8-133">Instalando o analisador de práticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="91ea8-133">Installing Best Practices Analyzer</span></span>

<span data-ttu-id="91ea8-134">Você pode baixar o analisador de práticas recomendadas para o Lync Server 2013 em [https://go.microsoft.com/fwlink/p/?linkId=266539](https://go.microsoft.com/fwlink/p/?linkid=266539) .</span><span class="sxs-lookup"><span data-stu-id="91ea8-134">You can download the Best Practices Analyzer for Lync Server 2013 at [https://go.microsoft.com/fwlink/p/?linkId=266539](https://go.microsoft.com/fwlink/p/?linkid=266539).</span></span>

<span data-ttu-id="91ea8-135">Para instalar o analisador de práticas recomendadas, inicie o arquivo do Microsoft Installer RtcBPA.msi no computador onde você deseja instalar a ferramenta e siga as instruções na tela.</span><span class="sxs-lookup"><span data-stu-id="91ea8-135">To install Best Practices Analyzer, start the Microsoft Installer file RtcBPA.msi on the computer where you want to install the tool, and then follow the instructions on the screen.</span></span> <span data-ttu-id="91ea8-136">O local padrão para a instalação dos arquivos de programa é os \<system drive\> \\ arquivos de programas do \\ Lync Server 2013 \\ BPA.</span><span class="sxs-lookup"><span data-stu-id="91ea8-136">The default location for installing the program files is \<system drive\>\\Program Files\\Lync Server 2013\\BPA.</span></span>

<span data-ttu-id="91ea8-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91ea8-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

