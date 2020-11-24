---
title: Configurar registros de DNS para implantação de pool piloto
description: Configurar registros DNS para a implantação do pool piloto.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS records for pilot pool deployment
ms:assetid: eb421bad-4bf1-4837-a077-7795094692d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721921(v=OCS.15)
ms:contentKeyID: 49733855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e41e163432ba910f6d083cc508e8ad8c9f2006d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390013"
---
# <a name="configure-dns-records-for-pilot-pool-deployment"></a><span data-ttu-id="f757e-103">Configurar registros de DNS para implantação de pool piloto</span><span class="sxs-lookup"><span data-stu-id="f757e-103">Configure DNS records for pilot pool deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f757e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f757e-104">

<span> </span></span></span>

<span data-ttu-id="f757e-105">_**Tópico da última modificação:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="f757e-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="f757e-106">Antes de implantar o pool piloto do Lync Server 2013, você deve atualizar as entradas do host DNS a para o pool piloto.</span><span class="sxs-lookup"><span data-stu-id="f757e-106">Prior to deploying the Lync Server 2013 pilot pool, you must update the DNS Host A entries for the pilot pool.</span></span> <span data-ttu-id="f757e-107">Para concluir esse procedimento com êxito, você deve estar conectado ao servidor ou ao domínio como membro do grupo Domain admins ou de um membro do grupo DnsAdmins.</span><span class="sxs-lookup"><span data-stu-id="f757e-107">To successfully complete this procedure, you should be logged on to the server or domain as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="f757e-108">**Para configurar registros do host DNS A**</span><span class="sxs-lookup"><span data-stu-id="f757e-108">**To configure DNS Host A records**</span></span>

1.  <span data-ttu-id="f757e-109">No servidor DNS (sistema de nomes de domínio), clique em **Iniciar**, clique em **Ferramentas administrativas** e clique em **DNS**.</span><span class="sxs-lookup"><span data-stu-id="f757e-109">On the Domain Name System (DNS) server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="f757e-110">Na árvore de console do seu domínio, expanda **zonas de pesquisa direta** e clique com o botão direito do mouse no domínio no qual o Lync Server 2013 será instalado.</span><span class="sxs-lookup"><span data-stu-id="f757e-110">In the console tree for your domain, expand **Forward Lookup Zones**, and then right-click the domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="f757e-111">Clique em **novo host (A ou aaaa)**.</span><span class="sxs-lookup"><span data-stu-id="f757e-111">Click **New Host (A or AAAA)**.</span></span>

4.  <span data-ttu-id="f757e-112">Clique em **nome**, digite o nome do host do pool do Lync Server 2013 (o nome do domínio é presumido na zona em que o registro é definido e não precisa ser inserido como parte do registro a).</span><span class="sxs-lookup"><span data-stu-id="f757e-112">Click **Name**, type the host name for the Lync Server 2013 pool (the domain name is assumed from the zone that the record is defined in and does not need to be entered as part of the A record).</span></span>

5.  <span data-ttu-id="f757e-113">Clique em **endereço IP**, digite o endereço IP do pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="f757e-113">Click **IP Address**, type the IP address for the Front End pool.</span></span>

6.  <span data-ttu-id="f757e-114">Clique em **Adicionar host** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f757e-114">Click **Add Host**, and then click **OK**.</span></span>

7.  <span data-ttu-id="f757e-115">Quando terminar, clique em **concluído**.</span><span class="sxs-lookup"><span data-stu-id="f757e-115">When you are finished, click **Done**.</span></span>

<span data-ttu-id="f757e-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f757e-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

