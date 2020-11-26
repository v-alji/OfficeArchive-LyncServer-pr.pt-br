---
title: 'Lync Server 2013: Requisitos técnicos para bypass de mídia'
description: 'Lync Server 2013: requisitos técnicos para bypass de mídia.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for media bypass
ms:assetid: 6162a204-0e7c-460a-8eb2-e592c6590a8a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398435(v=OCS.15)
ms:contentKeyID: 48184321
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dee594139031966342fcec2bc1296a603055b4cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423432"
---
# <a name="technical-requirements-for-media-bypass-in-lync-server-2013"></a><span data-ttu-id="2c5f7-103">Requisitos técnicos para bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2c5f7-103">Technical requirements for media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2c5f7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2c5f7-104">

<span> </span></span></span>

<span data-ttu-id="2c5f7-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="2c5f7-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="2c5f7-106">Para cada chamada à PSTN, o servidor de mediação determina se a mídia do ponto de extremidade do Lync da origem pode ser enviada diretamente para um ponto do servidor de mediação sem percorrer o servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="2c5f7-106">For each call to the PSTN, the Mediation Server determines whether media from the Lync endpoint of origin can be sent directly to a Mediation Server peer without traversing the Mediation Server.</span></span> <span data-ttu-id="2c5f7-107">O par pode ser um gateway PSTN, um IP-PBX ou um SBC (Controlador de Borda de Sessão) em um ITSP (provedor de serviços de telefonia da Internet) associado ao tronco entre o Servidor de Mediação para o qual a chamada é roteada.</span><span class="sxs-lookup"><span data-stu-id="2c5f7-107">The peer can be a PSTN gateway, IP-PBX, or Session Border Controller (SBC) at an Internet telephony service provider (ITSP) that is associated with the trunk between the Mediation Server where the call is routed.</span></span>

<span data-ttu-id="2c5f7-108">O bypass de mídia pode ser empregado quando os seguintes requisitos são atendidos:</span><span class="sxs-lookup"><span data-stu-id="2c5f7-108">Media bypass can be employed when the following requirements are met:</span></span>

  - <span data-ttu-id="2c5f7-109">Um peer do servidor de mediação deve dar suporte aos recursos necessários para o bypass de mídia, o mais importante é a capacidade de manipular várias respostas bifurcadas (conhecidas como "primeiras caixas de diálogo").</span><span class="sxs-lookup"><span data-stu-id="2c5f7-109">A Mediation Server peer must support the necessary capabilities for media bypass, the most important being the ability to handle multiple forked responses (known as “early dialogs”).</span></span> <span data-ttu-id="2c5f7-110">Contate o fabricante do seu gateway ou PBX ou seu ITSP para obter o valor do número máximo de caixas de diálogo iniciais que o gateway, o PBX ou o SBC pode aceitar.</span><span class="sxs-lookup"><span data-stu-id="2c5f7-110">Contact the manufacturer of your gateway or PBX, or your ITSP, to obtain the value for the maximum number of early dialogs that the gateway, PBX, or SBC can accept.</span></span>

  - <span data-ttu-id="2c5f7-111">O par do servidor de mediação deve aceitar o tráfego de mídia diretamente dos pontos de extremidade do Lync.</span><span class="sxs-lookup"><span data-stu-id="2c5f7-111">The Mediation Server peer must accept media traffic directly from Lync endpoints.</span></span> <span data-ttu-id="2c5f7-112">Muitos ITSPs permitem que o SBC receba tráfego somente do servidor de mediação.</span><span class="sxs-lookup"><span data-stu-id="2c5f7-112">Many ITSPs allow their SBC to receive traffic only from the Mediation Server.</span></span> <span data-ttu-id="2c5f7-113">Entre em contato com seu ITSP para determinar se o seu SBC aceita tráfego de mídia diretamente dos pontos de extremidade do Lync.</span><span class="sxs-lookup"><span data-stu-id="2c5f7-113">Contact your ITSP to determine whether its SBC accepts media traffic directly from Lync endpoints.</span></span>

  - <span data-ttu-id="2c5f7-114">Os clientes do Lync e um peer do servidor de mediação devem ser bem conectados, o que significa que eles estão localizados na mesma região de rede ou em sites de rede que se conectam à região em links de WAN que não têm restrições de largura de banda</span><span class="sxs-lookup"><span data-stu-id="2c5f7-114">Lync clients and a Mediation Server peer must be well connected, meaning that they are either located in the same network region or at network sites that connect to the region over WAN links that have no bandwidth constraints</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="2c5f7-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c5f7-115">See Also</span></span>


[<span data-ttu-id="2c5f7-116">Modos de bypass de mídia no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2c5f7-116">Media bypass modes in Lync Server 2013</span></span>](lync-server-2013-media-bypass-modes.md)  
[<span data-ttu-id="2c5f7-117">Bypass de mídia e controle de admissão de chamadas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2c5f7-117">Media bypass and call admission control in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-call-admission-control.md)  
  

<span data-ttu-id="2c5f7-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2c5f7-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

