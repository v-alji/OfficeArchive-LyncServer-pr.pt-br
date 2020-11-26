---
title: Pré-requisitos
description: Pré-requisitos.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prerequisites
ms:assetid: 48016bea-be3b-4ba5-8df8-d8ad4d9243d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945592(v=OCS.15)
ms:contentKeyID: 51541417
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 936e52961539ed57fe1b610d42fb1c9cf35589b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446401"
---
# <a name="prerequisites"></a><span data-ttu-id="853d3-103">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="853d3-103">Prerequisites</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="853d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="853d3-104">

<span> </span></span></span>

<span data-ttu-id="853d3-105">_**Tópico da última modificação:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="853d3-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="853d3-106">Há vários requisitos de configuração de hardware, software e sistema que você precisará para executar a ferramenta de stress e desempenho do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="853d3-106">There are various hardware, software, and system configuration requirements that you’ll need to run the Lync Server 2013 Stress and Performance Tool.</span></span>

<div>

## <a name="client-hardware-requirements"></a><span data-ttu-id="853d3-107">Requisitos de hardware do cliente</span><span class="sxs-lookup"><span data-stu-id="853d3-107">Client Hardware Requirements</span></span>

<span data-ttu-id="853d3-108">Para executar a ferramenta de stress e desempenho do Lync Server 2013 na sua implantação do Lync Server 2013 para cada usuário do 4.500 cuja carga você deseja simular, é preciso ter pelo menos um computador dedicado que atenda aos seguintes requisitos mínimos de hardware:</span><span class="sxs-lookup"><span data-stu-id="853d3-108">To run the Lync Server 2013 Stress and Performance Tool on your Lync Server 2013 deployment, for every 4,500 users whose load you want to simulate, you’ll need at least one dedicated computer that meets the following minimum hardware requirements:</span></span>

  - <span data-ttu-id="853d3-109">Adaptador rede de 1 gigabit</span><span class="sxs-lookup"><span data-stu-id="853d3-109">1 gigabit network adapter</span></span>

  - <span data-ttu-id="853d3-110">8 GB de RAM</span><span class="sxs-lookup"><span data-stu-id="853d3-110">8-GB ram</span></span>

  - <span data-ttu-id="853d3-111">2 unidades de processamento central de Dual-Core (CPUs)</span><span class="sxs-lookup"><span data-stu-id="853d3-111">2 dual-core central processing units (CPUs)</span></span>

</div>

<div>

## <a name="client-software-requirements"></a><span data-ttu-id="853d3-112">Requisitos de software do cliente</span><span class="sxs-lookup"><span data-stu-id="853d3-112">Client Software Requirements</span></span>

<span data-ttu-id="853d3-113">Para executar a ferramenta de stress e desempenho do Lync Server 2013 em sua implantação do Lync Server 2013, os sistemas operacionais com suporte são:</span><span class="sxs-lookup"><span data-stu-id="853d3-113">To run the Lync Server 2013 Stress and Performance Tool on your Lync Server 2013 deployment, the supported operating systems are:</span></span>

  - <span data-ttu-id="853d3-114">Sistema operacional Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="853d3-114">Windows Server 2012 operating system</span></span>

  - <span data-ttu-id="853d3-115">Sistema operacional Windows Server 2008 (edição de 64 bits)</span><span class="sxs-lookup"><span data-stu-id="853d3-115">Windows Server 2008 operating system (64-bit edition)</span></span>

<span data-ttu-id="853d3-116">O computador cliente deve atender aos seguintes requisitos de software:</span><span class="sxs-lookup"><span data-stu-id="853d3-116">Your client computer must meet the following software requirements:</span></span>

  - <span data-ttu-id="853d3-117">Você deve ter o [Microsoft .NET Framework 4,5](https://go.microsoft.com/fwlink/?linkid=143212) Runtime instalado.</span><span class="sxs-lookup"><span data-stu-id="853d3-117">You must have the [Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?linkid=143212) runtime installed.</span></span>

  - <span data-ttu-id="853d3-118">No Windows Server 2008/Windows Server 2012, o recurso experiência da área de trabalho deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="853d3-118">On Windows Server 2008/Windows Server 2012, the Desktop Experience feature must be enabled.</span></span>

  - <span data-ttu-id="853d3-119">Você deve ter instalado o [pacote redistribuível do Microsoft Visual C++ 2012](https://go.microsoft.com/fwlink/?linkid=143216) (x64).</span><span class="sxs-lookup"><span data-stu-id="853d3-119">You must have the [Microsoft Visual C++ 2012 redistributable package](https://go.microsoft.com/fwlink/?linkid=143216) (x64) installed.</span></span>

  - <span data-ttu-id="853d3-120">Uma implantação totalmente configurada do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="853d3-120">A fully configured Lync Server 2013 deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="853d3-121">As bibliotecas da API gerenciada de comunicação unificada da Microsoft (UCMA) 4,0 estão incluídas no pacote de instalação, portanto, o UCMA não é necessário e não deve ser instalado em computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="853d3-121">Microsoft Unified Communications Managed API (UCMA) 4.0 libraries are included in the installation package, so UCMA is not required and should not be installed on client computers.</span></span>



</div>

</div>

<div>

## <a name="configuration-requirements"></a><span data-ttu-id="853d3-122">Requisitos de configuração</span><span class="sxs-lookup"><span data-stu-id="853d3-122">Configuration Requirements</span></span>

<span data-ttu-id="853d3-123">Os computadores que executarão a ferramenta de stress e desempenho do Lync Server 2013 devem ser configurados de acordo com os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="853d3-123">The computers that will run the Lync Server 2013 Stress and Performance Tool must be configured according to the following requirements:</span></span>

1.  <span data-ttu-id="853d3-124">Você deve estar conectado como um membro do grupo domínio ou administradores locais.</span><span class="sxs-lookup"><span data-stu-id="853d3-124">You must be logged on as a member of the Domain or Local Admins group.</span></span>

2.  <span data-ttu-id="853d3-125">A ferramenta de stress e desempenho do Lync Server 2013 (LyncPerfTool.exe) não pode ser executada em um computador que também esteja executando os componentes do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="853d3-125">Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe) cannot be run on a computer that is also running Lync Server 2013 components.</span></span>

3.  <span data-ttu-id="853d3-126">Você deve executar a ferramenta de criação de usuários do Lync Server 2013 (UserProvisioningTool.exe) no servidor front-end ou no servidor Standard Edition, onde as contas de usuário residem.</span><span class="sxs-lookup"><span data-stu-id="853d3-126">You must run the Lync Server 2013 User Creation tool (UserProvisioningTool.exe) on the Front End Server or on the Standard Edition server where the user accounts will reside.</span></span> <span data-ttu-id="853d3-127">Quando a ferramenta é executada várias vezes, cada usuário habilitado para a comunicação unificada da Microsoft deve ter um número de telefone exclusivo.</span><span class="sxs-lookup"><span data-stu-id="853d3-127">When the tool is run multiple times, each user who is enabled for Microsoft Unified Communications must have a unique phone number.</span></span>

4.  <span data-ttu-id="853d3-128">O tamanho do arquivo da página deve ser gerenciado pelo sistema ou deve ter pelo menos 1,5 vezes a quantidade de RAM no sistema.</span><span class="sxs-lookup"><span data-stu-id="853d3-128">The page file size should be system-managed, or should be at least 1.5 times the amount of RAM on the system.</span></span>

<span data-ttu-id="853d3-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="853d3-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

