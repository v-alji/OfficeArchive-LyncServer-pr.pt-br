---
title: 'Lync Server 2013: criando a topologia usando a ferramenta de planejamento'
description: 'Lync Server 2013: criando a topologia usando a ferramenta de planejamento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Designing the topology by using the Planning Tool
ms:assetid: 2a352f62-c5cb-4ef1-9aa9-7f0c1ab47455
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558631(v=OCS.15)
ms:contentKeyID: 51541454
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fcc10d09d7b8b815e2b4924d06c10de23c14236b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429528"
---
# <a name="designing-the-topology-for-lync-server-2013-by-using-the-planning-tool"></a><span data-ttu-id="abe96-103">Criando a topologia do Lync Server 2013 usando a ferramenta de planejamento</span><span class="sxs-lookup"><span data-stu-id="abe96-103">Designing the topology for Lync Server 2013 by using the Planning Tool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abe96-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abe96-104">

<span> </span></span></span>

<span data-ttu-id="abe96-105">_**Tópico da última modificação:** 2013-03-04_</span><span class="sxs-lookup"><span data-stu-id="abe96-105">_**Topic Last Modified:** 2013-03-04_</span></span>

<span data-ttu-id="abe96-106">O Microsoft Lync Server 2013, ferramenta de planejamento é uma ferramenta de planejamento orientada por assistente que faz perguntas sobre a topologia do Lync Server 2013 que você está criando.</span><span class="sxs-lookup"><span data-stu-id="abe96-106">The Microsoft Lync Server 2013, Planning Tool is a wizard driven, interview-like tool that asks questions about the Lync Server 2013 topology that you are designing.</span></span> <span data-ttu-id="abe96-107">A ferramenta de planejamento usa as informações fornecidas, combinadas com práticas preferenciais de design e capacidade de topologia, para apresentar uma topologia recomendada com base nas respostas fornecidas.</span><span class="sxs-lookup"><span data-stu-id="abe96-107">The Planning Tool uses the information supplied, coupled with preferred practices for topology design and capacity, to present a recommended topology based on the answers supplied.</span></span> <span data-ttu-id="abe96-108">Você pode baixar a ferramenta de planejamento no centro de download da Microsoft ( [https://go.microsoft.com/fwlink/?LinkID=282725](https://go.microsoft.com/fwlink/?linkid=282725) ).</span><span class="sxs-lookup"><span data-stu-id="abe96-108">You can download the Planning Tool from the Microsoft Downloads Center ([https://go.microsoft.com/fwlink/?LinkID=282725](https://go.microsoft.com/fwlink/?linkid=282725)).</span></span>

<span data-ttu-id="abe96-109">Por fim, o objetivo da ferramenta de planejamento é facilitar a complexidade potencial de criar uma topologia completa do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="abe96-109">Ultimately, the goal of the Planning Tool is to ease the potential complexity of designing a complete Lync Server 2013 topology.</span></span> <span data-ttu-id="abe96-110">A ferramenta também fornece referências contextuais à documentação de planejamento e implantação dentro da ferramenta, contanto que uma conexão com a Internet esteja disponível para se conectar ao site Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="abe96-110">The tool also provides contextual references to planning and deployment documentation inside the tool, provided that an Internet connection is available to connect to the Microsoft TechNet website.</span></span>

<span data-ttu-id="abe96-111">Após personalizar a topologia com os endereços TCP/IP da infraestrutura e FQDNs (nomes de domínio totalmente qualificados), a ferramenta de planejamento disponibiliza uma série de relatórios que abrangem o nome DNS, as regras de firewall, os certificados e muito mais.</span><span class="sxs-lookup"><span data-stu-id="abe96-111">After customizing the topology with the infrastructure’s TCP/IP addresses and fully qualified domain names (FQDNs), the Planning Tool makes available a series of reports that cover Domain Name System (DNS) naming, firewall rules, certificates, and more.</span></span>

<span data-ttu-id="abe96-112">A ferramenta de planejamento também fornece a capacidade de exportar informações em dois formatos:</span><span class="sxs-lookup"><span data-stu-id="abe96-112">The Planning Tool also provides the ability to export information in two formats:</span></span>

  - <span data-ttu-id="abe96-113">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="abe96-113">Microsoft Excel</span></span>

  - <span data-ttu-id="abe96-114">Microsoft Visio</span><span class="sxs-lookup"><span data-stu-id="abe96-114">Microsoft Visio</span></span>

<span data-ttu-id="abe96-115">Os tópicos a seguir introduzem e detalham a ferramenta de planejamento.</span><span class="sxs-lookup"><span data-stu-id="abe96-115">The following topics introduce and detail the Planning Tool.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="abe96-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="abe96-116">In This Section</span></span>

  - [<span data-ttu-id="abe96-117">Instalando a Ferramenta de Planejamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abe96-117">Installing the Planning Tool in Lync Server 2013</span></span>](lync-server-2013-installing-the-planning-tool.md)

  - [<span data-ttu-id="abe96-118">Instalação de software opcional no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abe96-118">Installing optional software in Lync Server 2013</span></span>](lync-server-2013-installing-optional-software.md)

  - [<span data-ttu-id="abe96-119">Navegar pela ferramenta de planejamento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abe96-119">Navigating the Planning Tool in Lync Server 2013</span></span>](lync-server-2013-navigating-the-planning-tool.md)

  - [<span data-ttu-id="abe96-120">Criar o design de topologia inicial para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abe96-120">Create the initial topology design for Lync Server 2013</span></span>](lync-server-2013-create-the-initial-topology-design.md)

  - [<span data-ttu-id="abe96-121">Revisando os Relatórios do Administrador no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abe96-121">Reviewing the Administrator Reports in Lync Server 2013</span></span>](lync-server-2013-reviewing-the-administrator-reports.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="abe96-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="abe96-122">See Also</span></span>


[<span data-ttu-id="abe96-123">Implantando o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abe96-123">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
[<span data-ttu-id="abe96-124">Planejamento de Servidores Front-End, sistema de mensagens instantâneas e presença no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abe96-124">Planning for Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>](lync-server-2013-planning-for-front-end-servers-instant-messaging-and-presence.md)  
  

<span data-ttu-id="abe96-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abe96-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

