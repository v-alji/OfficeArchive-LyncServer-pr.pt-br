---
title: 'Lync Server 2013: Visão Geral do Diretor'
description: 'Lync Server 2013: visão geral do diretor.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of the Director
ms:assetid: cf9919b3-e16b-47c5-be1d-2c4bc64f44ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398879(v=OCS.15)
ms:contentKeyID: 48185393
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6686534e22bab5b02a2663789298e4cf7ea582c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424706"
---
# <a name="overview-of-the-director-in-lync-server-2013"></a><span data-ttu-id="07130-103">Visão Geral do Diretor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="07130-103">Overview of the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="07130-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="07130-104">

<span> </span></span></span>

<span data-ttu-id="07130-105">_**Tópico da última modificação:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="07130-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="07130-106">Um diretor é um servidor que executa o Lync Server 2013 que autentica solicitações do usuário, mas não hospeda nenhuma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="07130-106">A Director is a server running Lync Server 2013 that authenticates user requests, but does not home any user accounts.</span></span> <span data-ttu-id="07130-107">Opcionalmente, você pode implantar um diretor nos dois cenários a seguir:</span><span class="sxs-lookup"><span data-stu-id="07130-107">You optionally can deploy a Director in the following two scenarios:</span></span>

  - <span data-ttu-id="07130-108">Se você habilitar o acesso por usuários externos implantando servidores de borda, também deverá implantar um diretor.</span><span class="sxs-lookup"><span data-stu-id="07130-108">If you enable access by external users by deploying Edge Servers, you should also deploy a Director.</span></span> <span data-ttu-id="07130-109">Nesse cenário, o diretor autentica os usuários externos e, em seguida, passa o tráfego deles para servidores internos.</span><span class="sxs-lookup"><span data-stu-id="07130-109">In this scenario, the Director authenticates the external users, and then passes their traffic on to internal servers.</span></span> <span data-ttu-id="07130-110">Quando um diretor é usado para autenticar usuários externos, ele libera os servidores de pool de front-end da sobrecarga de execução de autenticação desses usuários.</span><span class="sxs-lookup"><span data-stu-id="07130-110">When a Director is used to authenticate external users, it relieves Front End pool servers from the overhead of performing authentication of these users.</span></span> <span data-ttu-id="07130-111">Também ajuda a proteger pools de front-end internos contra tráfego mal-intencionado, como ataques de negação de serviço.</span><span class="sxs-lookup"><span data-stu-id="07130-111">It also helps insulate internal Front End pools from malicious traffic such as denial-of-service attacks.</span></span> <span data-ttu-id="07130-112">Se a rede estiver inundada com tráfego externo inválido nesse tipo de ataque, esse tráfego terminará no diretor.</span><span class="sxs-lookup"><span data-stu-id="07130-112">If the network is flooded with invalid external traffic in such an attack, this traffic ends at the Director.</span></span>

  - <span data-ttu-id="07130-113">Se você implantar vários pools de front-end em um site central, adicionando um diretor ao site, você pode simplificar solicitações de autenticação e melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="07130-113">If you deploy multiple Front End pools at a central site, by adding a Director to that site you can streamline authentication requests and improve performance.</span></span> <span data-ttu-id="07130-114">Nesse cenário, todas as solicitações entram primeiro no director, que, em seguida, as roteia para o pool de front-end correto.</span><span class="sxs-lookup"><span data-stu-id="07130-114">In this scenario, all requests go first to the Director, which then routes them to the correct Front End pool.</span></span>

<span data-ttu-id="07130-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="07130-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

