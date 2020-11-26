---
title: 'Lync Server 2013: Decidindo como implantar o Microsoft Lync'
description: 'Lync Server 2013: decidindo como implantar o Microsoft Lync.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deciding how to deploy Microsoft Lync
ms:assetid: 6ca677d3-745d-4935-8f05-19274a8bccf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204979(v=OCS.15)
ms:contentKeyID: 48184423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a800b51dfddc6f2c99e42c8f117056ed4091b6a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431229"
---
# <a name="deciding-how-to-deploy-lync-server-2013"></a><span data-ttu-id="9d4ba-103">Decidindo como implantar o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9d4ba-103">Deciding how to deploy Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d4ba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d4ba-104">

<span> </span></span></span>

<span data-ttu-id="9d4ba-105">_**Tópico da última modificação:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="9d4ba-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="9d4ba-106">Ao planejar o Lync, a primeira decisão importante é como implantar o Microsoft Lync: como o Lync Server 2013 local ou o Lync Online com o Microsoft 365 ou o Office 365 na nuvem.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-106">When planning for Lync, the first major decision is how to deploy Microsoft Lync: as Lync Server 2013 on premises, or Lync Online with Microsoft 365 or Office 365 in the cloud.</span></span>

  - <span data-ttu-id="9d4ba-107">**Lync Server 2013 local** : esta opção fornece o conjunto de recursos completo do Lync e fornece a flexibilidade máxima para configurar, personalizar e operar a implantação.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-107">**Lync Server 2013 on-premises** : This choice provides the complete Lync feature set and provides ultimate flexibility in configuring, customizing, and operating your deployment.</span></span> <span data-ttu-id="9d4ba-108">Todos os servidores são instalados no local e mantidos pela sua organização.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-108">All servers are installed onsite and maintained by your organization.</span></span> <span data-ttu-id="9d4ba-109">Uma implantação local fornece a gama completa de recursos do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-109">An on-premises deployment provides the full range of Lync Server features.</span></span>

  - <span data-ttu-id="9d4ba-110">**Lync Online na nuvem** O Lync Online foi projetado para organizações que desejam os benefícios de custo e agilidade das mensagens instantâneas, presença e reuniões em nuvem sem sacrificar os recursos de classe empresarial do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-110">**Lync Online in the cloud** Lync Online is designed for organizations that want the cost and agility benefits of cloud-based instant messaging, presence, and meetings without sacrificing the business-class capabilities of Lync Server.</span></span> <span data-ttu-id="9d4ba-111">Com o Lync Online, a Microsoft implanta e mantém a infraestrutura de servidor necessária e manipula manutenção, patches e atualizações contínuas.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-111">With Lync Online, Microsoft deploys and maintains the required server infrastructure, and handles ongoing maintenance, patches, and upgrades.</span></span> <span data-ttu-id="9d4ba-112">Alguns recursos disponíveis em uma implantação local não estão disponíveis no Lync Online.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-112">Some features available in an on-premises deployment are not available in Lync Online.</span></span>

<span data-ttu-id="9d4ba-113">Qual tipo de implantação seria melhor para você depende das cargas de trabalho que você deseja implantar e o status geográfico e comercial da sua organização.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-113">Which type of deployment would be best for you depends on the workloads you want to deploy, and your organization’s geographical and business status.</span></span>

<div>

## <a name="lync-server"></a><span data-ttu-id="9d4ba-114">Servidor Lync</span><span class="sxs-lookup"><span data-stu-id="9d4ba-114">Lync Server</span></span>

<span data-ttu-id="9d4ba-115">Uma implantação do Lync Server local é melhor para os seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="9d4ba-115">An on-premises Lync Server deployment is best for the following scenarios:</span></span>

  - <span data-ttu-id="9d4ba-116">**Recursos completos do Enterprise Voice**   Se você planeja implantar uma solução completa Enterprise Voice para substituir seu PBX ou que usa recursos de chamada avançada, uma implantação do Lync Server local será necessária.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-116">**Full Enterprise Voice Capabilities**   If you plan to deploy a full Enterprise Voice solution to replace your PBX or which uses advanced calling features, an on-premises Lync Server deployment is required.</span></span> <span data-ttu-id="9d4ba-117">O local é compatível com a conectividade direta com sistemas PBX e troncos e recursos de telefone avançados, como grupos de resposta e estacionamento de chamadas.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-117">On-premises supports direct connectivity with PBX systems and trunks, and advanced phone features such as response groups and call park.</span></span> <span data-ttu-id="9d4ba-118">No momento, o Lync Online não oferece suporte a esses recursos.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-118">Lync Online does not currently support these features.</span></span>

  - <span data-ttu-id="9d4ba-119">**Controles de qualidade de mídia**   Se você quiser uma gama completa de recursos de garantia de qualidade de mídia, como o controle de admissão de chamadas (CAC) e os recursos de qualidade do serviço (QoS), será necessário uma implantação local.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-119">**Media Quality Controls**   If you want the full range of media quality assurance features, such as Call Admission Control (CAC) and Quality of Service (QoS) features, you will want an on-premises deployment .</span></span>

  - <span data-ttu-id="9d4ba-120">**Chat persistente**   Se precisar implantar o chat persistente para a sua organização, você deverá escolher uma implantação local.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-120">**Persistent Chat**   If you need to deploy Persistent chat for your organization, you must choose an on-premises deployment.</span></span>

  - <span data-ttu-id="9d4ba-121">**aplicativos de servidor de terceiros**   Somente implantações locais podem funcionar com aplicativos de terceiros confiáveis que usam a API gerenciada de comunicação unificada da Microsoft (UCMA).</span><span class="sxs-lookup"><span data-stu-id="9d4ba-121">**3rd-Party Server Applications**   Only on-premises deployments can work with trusted 3rd-party applications that use the Microsoft Unified Communications Managed API (UCMA).</span></span>

  - <span data-ttu-id="9d4ba-122">**Empresas multinacionais/de várias regiões que precisam de suporte regional**   Se você tiver datacenters em vários países ou regiões e precisar que os servidores sejam implantados e gerenciados de forma regional, uma implantação local será melhor, pois oferece esse tipo de recursos de gerenciamento regional.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-122">**Multi-National/Multi-Regional Companies Needing Regional Support**   If you have datacenters in multiple countries or regions and need servers to be deployed and managed on a regional basis, an on-premises deployment is best, as it provides this type of regional management capabilities.</span></span>

  - <span data-ttu-id="9d4ba-123">**Controle completo sobre políticas, relatórios e atualizações**   Com uma implantação local do Lync Server, você tem acesso ao conjunto completo de políticas de servidor e de cliente, monitoramento e outros relatórios e tempo de atualização.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-123">**Complete control over policies, reports, and upgrades**   With an on premises Lync Server deployment, you have access to the full set of server and client policies, Monitoring and other reports, and timing of upgrades.</span></span> <span data-ttu-id="9d4ba-124">O Lync Online fornece um subconjunto de relatórios e configurações de política e fornece uma janela limitada, embora significativa, para aceitar atualizações.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-124">Lync Online provides a subset of policy setting and reports, and provides a limited, though significant, window for accepting upgrades.</span></span>

</div>

<div>

## <a name="lync-online"></a><span data-ttu-id="9d4ba-125">Lync Online</span><span class="sxs-lookup"><span data-stu-id="9d4ba-125">Lync Online</span></span>

<span data-ttu-id="9d4ba-126">Se nenhum dos fatores na lista anterior for essencial para você, talvez você queira escolher o Lync Online, para implantação e gerenciamento mais simples.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-126">If none of the factors in the preceding list are critical for you, you may want to choose Lync Online, for simpler deployment and manageability.</span></span> <span data-ttu-id="9d4ba-127">O Lync Online oferece um conjunto robusto de recursos de chat, presença e conferência e também permite chamadas de voz e vídeo por IP entre os usuários da sua organização.</span><span class="sxs-lookup"><span data-stu-id="9d4ba-127">Lync Online provides a robust IM, presence and conferencing feature set, and also enables voice and video calls over IP between users in your organization.</span></span>

<span data-ttu-id="9d4ba-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d4ba-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
