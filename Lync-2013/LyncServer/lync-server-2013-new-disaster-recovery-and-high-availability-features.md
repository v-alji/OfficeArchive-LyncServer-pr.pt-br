---
title: 'Lync Server 2013: Novos recursos de recuperação de desastre e alta disponibilidade'
description: 'Lync Server 2013: novos recursos de recuperação de desastres e alta disponibilidade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New disaster recovery and high availability features
ms:assetid: 4fa7cd0f-784b-4d3f-b839-432c2ecaf7c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204892(v=OCS.15)
ms:contentKeyID: 48184130
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92816f61b66d9eed76c16286aaa6c7392dca7708
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425106"
---
# <a name="new-disaster-recovery-and-high-availability-features-in-lync-server-2013"></a><span data-ttu-id="583b7-103">Novos recursos de recuperação de desastre e alta disponibilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="583b7-103">New disaster recovery and high availability features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="583b7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="583b7-104">

<span> </span></span></span>

<span data-ttu-id="583b7-105">_**Tópico da última modificação:** 2012-09-20_</span><span class="sxs-lookup"><span data-stu-id="583b7-105">_**Topic Last Modified:** 2012-09-20_</span></span>

<span data-ttu-id="583b7-106">Como no Lync Server 2010, o principal esquema de alta disponibilidade (HA) do Lync Server 2013 é baseado na redundância do servidor via pool.</span><span class="sxs-lookup"><span data-stu-id="583b7-106">As in Lync Server 2010, the main high availability (HA) scheme for Lync Server 2013 is based on server redundancy via pooling.</span></span> <span data-ttu-id="583b7-107">Se um servidor que executa determinada função falhar, os demais servidores do pool que executam a mesma função assumirão a carga desse servidor.</span><span class="sxs-lookup"><span data-stu-id="583b7-107">If a server running a certain server role fails, the other servers in the pool running the same role take the load of that server.</span></span> <span data-ttu-id="583b7-108">Isso se aplica a Servidores Front-End, Servidores de Borda, Servidores de Mediação e Diretores.</span><span class="sxs-lookup"><span data-stu-id="583b7-108">This applies to Front End Servers, Edge Servers, Mediation Servers, and Directors.</span></span>

<span data-ttu-id="583b7-109">O Lync Server 2013 adiciona novas medidas de recuperação de desastres permitindo que você emparelhe pools de front-end localizados em dois datacenters.</span><span class="sxs-lookup"><span data-stu-id="583b7-109">Lync Server 2013 adds new disaster recovery measures by enabling you to pair Front End pools located in two datacenters.</span></span> <span data-ttu-id="583b7-110">Se um dos pools emparelhados ficar inativo, um administrador poderá fazer failover dos usuários desse pool para o outro pool do par, para dar continuidade ao serviço.</span><span class="sxs-lookup"><span data-stu-id="583b7-110">If one of the paired pools goes down, an administrator can fail over the users from that pool to the other pool in the pair, to provide continuation of service.</span></span> <span data-ttu-id="583b7-111">Essa funcionalidade não requer soluções caras de rede ou hardware, como redes de armazenamento ou discos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="583b7-111">This functionality does not require expensive network or hardware solutions such as storage networks or shared disks.</span></span>

<span data-ttu-id="583b7-112">O Lync Server 2013 também adiciona alta disponibilidade do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="583b7-112">Lync Server 2013 also adds Back End Server high availability.</span></span> <span data-ttu-id="583b7-113">Esta é uma topologia opcional na qual você implanta dois servidores back-end para um pool de front-end e configura o espelhamento do SQL síncrono para todos os bancos de dados do Lync em execução nos servidores de back-end.</span><span class="sxs-lookup"><span data-stu-id="583b7-113">This is an optional topology in which you deploy two Back End Servers for a Front End pool, and set up synchronous SQL mirroring for all the Lync databases running on the Back End Servers.</span></span> <span data-ttu-id="583b7-114">Você pode escolher se deseja implantar uma testemunha para o espelho.</span><span class="sxs-lookup"><span data-stu-id="583b7-114">You may choose whether to deploy a witness for the mirror.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="583b7-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="583b7-115">See Also</span></span>


[<span data-ttu-id="583b7-116">Planejamento para alta disponibilidade e recuperação de desastre no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="583b7-116">Planning for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
  

<span data-ttu-id="583b7-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="583b7-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

