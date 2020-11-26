---
title: 'Lync Server 2013: visão geral do analisador de práticas recomendadas'
description: 'Lync Server 2013: visão geral do analisador de práticas recomendadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Best Practices Analyzer
ms:assetid: c5fcaa05-eb1c-4092-90ad-177b127e795b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591349(v=OCS.15)
ms:contentKeyID: 48185364
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0ea48e88b26fa1081e5770fef2ac24efc21b74cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445152"
---
# <a name="overview-of-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="48558-103">Visão geral do analisador de práticas recomendadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="48558-103">Overview of Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="48558-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="48558-104">

<span> </span></span></span>

<span data-ttu-id="48558-105">_**Tópico da última modificação:** 2012-09-19_</span><span class="sxs-lookup"><span data-stu-id="48558-105">_**Topic Last Modified:** 2012-09-19_</span></span>

<span data-ttu-id="48558-106">Você pode usar o Lync Server 2013, o analisador de práticas recomendadas para identificar e resolver problemas com a implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48558-106">You can use Lync Server 2013, Best Practices Analyzer to identify and resolve problems with your Lync Server 2013 deployment.</span></span> <span data-ttu-id="48558-107">O Lync Server 2013, o analisador de práticas recomendadas coleta informações de configuração dos componentes do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48558-107">The Lync Server 2013, Best Practices Analyzer gathers configuration information from Lync Server 2013 components.</span></span>

<span data-ttu-id="48558-108">Com o acesso à rede adequado, o analisador de práticas recomendadas pode examinar servidores que executam os serviços de domínio do Active Directory, o Exchange Server Unified Messaging (UM) e o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48558-108">With the proper network access, the Best Practices Analyzer can examine servers running Active Directory Domain Services, Exchange Server Unified Messaging (UM), and Lync Server 2013.</span></span> <span data-ttu-id="48558-109">Você pode usar o analisador de práticas recomendadas para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="48558-109">You can use Best Practices Analyzer to do the following:</span></span>

  - <span data-ttu-id="48558-110">Fazer verificações proativas, verificando se a configuração está definida de acordo com as práticas recomendadas.</span><span class="sxs-lookup"><span data-stu-id="48558-110">Proactively perform checks, verifying that the configuration is set according to recommended best practices.</span></span>

  - <span data-ttu-id="48558-111">Detectar automaticamente as atualizações necessárias ao Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48558-111">Automatically detect required updates to Lync Server 2013.</span></span>

  - <span data-ttu-id="48558-112">Gere uma lista de problemas, como configurações de configuração otimizadas, opções sem suporte, atualizações ausentes ou práticas que não recomendamos.</span><span class="sxs-lookup"><span data-stu-id="48558-112">Generate a list of issues, such as suboptimal configuration settings, unsupported options, missing updates, or practices that we do not recommend.</span></span>

  - <span data-ttu-id="48558-113">Ajudar você a solucionar problemas e corrigir problemas específicos.</span><span class="sxs-lookup"><span data-stu-id="48558-113">Help you troubleshoot and fix specific problems.</span></span>

<span data-ttu-id="48558-114">O analisador de práticas recomendadas oferece os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="48558-114">Best Practices Analyzer provides the following features:</span></span>

  - <span data-ttu-id="48558-115">Pré-requisitos mínimos de instalação.</span><span class="sxs-lookup"><span data-stu-id="48558-115">Minimal installation prerequisites.</span></span>

  - <span data-ttu-id="48558-116">Documentação online sobre problemas relatados, incluindo dicas de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="48558-116">Online documentation about reported issues, including troubleshooting tips.</span></span>

  - <span data-ttu-id="48558-117">Informações de configuração que você pode salvar para ver mais tarde.</span><span class="sxs-lookup"><span data-stu-id="48558-117">Configuration information that you can save for later review.</span></span>

  - <span data-ttu-id="48558-118">Análise do sistema de ponta.</span><span class="sxs-lookup"><span data-stu-id="48558-118">State-of-the-art system analysis.</span></span>

<span data-ttu-id="48558-119">O analisador de práticas recomendadas usa um conjunto de arquivos de configuração XML para determinar as informações a serem coletadas do seu ambiente do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48558-119">Best Practices Analyzer uses a set of XML configuration files to determine the information to gather from your Lync Server 2013 environment.</span></span> <span data-ttu-id="48558-120">Além de verificar os serviços de domínio do Active Directory, ele verifica fontes como o registro do sistema operacional do Windows Server e as configurações na instrumentação de gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="48558-120">In addition to checking Active Directory Domain Services, it checks sources such as the Windows Server operating system registry and settings in Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="48558-121">O analisador de práticas recomendadas compara os dados que coleta com um conjunto de regras predefinidas para as configurações e configurações das implantações do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48558-121">Best Practices Analyzer compares the data it gathers with a set of predefined rules for the settings and configurations of Lync Server 2013 deployments.</span></span>

<span data-ttu-id="48558-122">Após comparar os dados coletados com as regras predefinidas, a ferramenta relata problemas.</span><span class="sxs-lookup"><span data-stu-id="48558-122">After comparing the collected data with the predefined rules, the tool reports issues.</span></span> <span data-ttu-id="48558-123">Para cada edição que ele relata, o analisador de práticas recomendadas fornece informações sobre o que foi encontrado no ambiente do Lync Server 2013 verificado e a configuração recomendada.</span><span class="sxs-lookup"><span data-stu-id="48558-123">For every issue that it reports, Best Practices Analyzer provides information about what was found in the scanned Lync Server 2013 environment and the recommended configuration.</span></span> <span data-ttu-id="48558-124">O analisador de práticas recomendadas também fornece links para informações mais detalhadas sobre os problemas específicos.</span><span class="sxs-lookup"><span data-stu-id="48558-124">Best Practices Analyzer also provides links to more detailed information about the specific issues.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="48558-125">O Lync Server 2013, o analisador de práticas recomendadas coleta informações de configuração somente de componentes do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="48558-125">The Lync Server 2013, Best Practices Analyzer gathers configuration information only from Lync Server 2013 components.</span></span> <span data-ttu-id="48558-126">Você pode usar as versões anteriores da ferramenta para verificar os ambientes anteriores.</span><span class="sxs-lookup"><span data-stu-id="48558-126">You can use the previous versions of the tool to scan previous environments.</span></span> <span data-ttu-id="48558-127">Para obter detalhes, consulte <A href="lync-server-2013-requirements-for-running-best-practices-analyzer.md">requisitos para a execução do analisador de práticas recomendadas no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="48558-127">For details, see <A href="lync-server-2013-requirements-for-running-best-practices-analyzer.md">Requirements for running Best Practices Analyzer in Lync Server 2013</A>.</span></span>



<span data-ttu-id="48558-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="48558-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

