---
title: 'Lync Server 2013: topologias para telefones IP'
description: 'Lync Server 2013: topologias para telefones IP.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topologies for IP phones
ms:assetid: 26ebffcf-43ff-4e70-847d-0fbc90e94e57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425740(v=OCS.15)
ms:contentKeyID: 48183662
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7a151a83a69e1f7e14dcbed8d8ab1038157fa839
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439655"
---
# <a name="topologies-for-ip-phones-in-lync-server-2013"></a><span data-ttu-id="cef09-103">Topologias para telefones IP no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cef09-103">Topologies for IP phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cef09-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cef09-104">

<span> </span></span></span>

<span data-ttu-id="cef09-105">_**Tópico da última modificação:** 2012-06-21_</span><span class="sxs-lookup"><span data-stu-id="cef09-105">_**Topic Last Modified:** 2012-06-21_</span></span>

<span data-ttu-id="cef09-106">Esta seção fornece uma visão geral do processo de conectividade e explica as diferenças entre como um telefone IP se conecta a uma rede interna e externa.</span><span class="sxs-lookup"><span data-stu-id="cef09-106">This section provides an overview of the connectivity process and explains the differences between how an IP phone connects in an internal and external network.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cef09-107">O Lync Server oferece suporte para os seguintes telefones IP: o Aastra 6721ip Common Area Phone, Aastra 6725ip Desk Phone, HP 4110 IP Phone (Common Area Phone), HP 4120 IP Phone (Phone Desk), Polycom CX600 IP Desk Phone, Polycom CX700 IP Desk Phone, Polycom CX500 IP Common Area Phone e Polycom CX3000 IP Conference Phone.</span><span class="sxs-lookup"><span data-stu-id="cef09-107">Lync Server provides support for the following IP phones: the Aastra 6721ip common area phone, Aastra 6725ip desk phone, HP 4110 IP Phone (common area phone), HP 4120 IP Phone (desk phone), Polycom CX600 IP desk phone, Polycom CX700 IP desk phone, Polycom CX500 IP common area phone, and Polycom CX3000 IP conference phone.</span></span> <span data-ttu-id="cef09-108">Desses telefones, tudo menos o Polycom CX700 pode executar o Lync Phone Edition.</span><span class="sxs-lookup"><span data-stu-id="cef09-108">Of those phones, all but the Polycom CX700 can run Lync Phone Edition.</span></span>



</div>

<span data-ttu-id="cef09-109">O diagrama a seguir descreve todos os componentes envolvidos na conectividade do dispositivo no ambiente corporativo.</span><span class="sxs-lookup"><span data-stu-id="cef09-109">The following diagram describes all the components involved in device connectivity within the corporate environment.</span></span>

<span data-ttu-id="cef09-110">**Topologia interna**</span><span class="sxs-lookup"><span data-stu-id="cef09-110">**Internal Topology**</span></span>

<span data-ttu-id="cef09-111">![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")</span><span class="sxs-lookup"><span data-stu-id="cef09-111">![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cef09-112">A figura anterior é uma representação lógica, não uma visão geral física.</span><span class="sxs-lookup"><span data-stu-id="cef09-112">The previous figure is a logical representation, not a physical overview.</span></span> <span data-ttu-id="cef09-113">Por exemplo, os serviços de domínio Active Directory (AD DS) raramente estão localizados na mesma máquina que qualquer componente do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="cef09-113">For example, Active Directory Domain Services (AD DS) is rarely located on the same machine as any Lync Server components.</span></span> <span data-ttu-id="cef09-114">O repositório de usuários pode estar localizado no servidor back-end ou nos servidores de arquivamento e monitoramento.</span><span class="sxs-lookup"><span data-stu-id="cef09-114">The user store can be located on the Back End Server or on the Archiving and Monitoring Servers.</span></span> <span data-ttu-id="cef09-115">O Shell de gerenciamento do Lync Server, o servidor Web e os serviços de atualização são parte da função de servidor front-end.</span><span class="sxs-lookup"><span data-stu-id="cef09-115">The Lync Server Management Shell, web server, and update services are all part of the Front End Server role.</span></span>



</div>

<span data-ttu-id="cef09-116">O diagrama a seguir fornece uma visão geral dos componentes envolvidos quando o dispositivo está localizado fora da rede corporativa.</span><span class="sxs-lookup"><span data-stu-id="cef09-116">The following diagram provides an overview of the components involved when the device is located outside the corporate network.</span></span>

<span data-ttu-id="cef09-117">**Topologia externa**</span><span class="sxs-lookup"><span data-stu-id="cef09-117">**External Topology**</span></span>

<span data-ttu-id="cef09-118">![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")</span><span class="sxs-lookup"><span data-stu-id="cef09-118">![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cef09-119">O serviço Web de atualização de dispositivo fornece um site externo e externo, mas somente o externo é mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="cef09-119">The Device Update Web service provides an external and internal website, but only the external one is shown here.</span></span><BR><span data-ttu-id="cef09-120">A localização do registrador e a URL do serviço Web de atualização de dispositivo para a organização devem ser publicadas no DNS se o acesso externo estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="cef09-120">The location of the Registrar and the URL of the Device Update Web service for the organization must be published in DNS if external access is to be enabled.</span></span> <span data-ttu-id="cef09-121">Além disso, o servidor de borda deve ser implantado e configurado corretamente para permitir comunicações externas do dispositivo para o ambiente corporativo e para trás.</span><span class="sxs-lookup"><span data-stu-id="cef09-121">Additionally, the Edge Server must be deployed and correctly configured to allow external communications from the device to the corporate environment and back.</span></span> <span data-ttu-id="cef09-122">Isso é omitido do diagrama anterior porque a implantação de borda não é específica da conectividade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cef09-122">This is omitted from the previous diagram because Edge deployment is not specific to device connectivity.</span></span>



<span data-ttu-id="cef09-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cef09-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

