---
title: 'Lync Server 2013: requisitos de DNS para mobilidade'
description: 'Lync Server 2013: requisitos de DNS para mobilidade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for mobility
ms:assetid: df6962bc-2a16-440e-a333-022ebd14f957
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690040(v=OCS.15)
ms:contentKeyID: 48185624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e2a8377dc7c856bb7250817cb3b8b66ed7789d3b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437802"
---
# <a name="dns-requirements-for-mobility-with-lync-server-2013"></a><span data-ttu-id="0fc5f-103">Requisitos de DNS para mobilidade com o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0fc5f-103">DNS requirements for mobility with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0fc5f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0fc5f-104">

<span> </span></span></span>

<span data-ttu-id="0fc5f-105">_**Tópico da última modificação:** 2012-11-13_</span><span class="sxs-lookup"><span data-stu-id="0fc5f-105">_**Topic Last Modified:** 2012-11-13_</span></span>

<span data-ttu-id="0fc5f-106">Ao implantar o recurso de mobilidade do Lync Server 2013, você pode usar as novas URLs disponíveis com o serviço de descoberta automática do Microsoft Lync Server 2013 ou pode usar suas URLs de serviços Web existentes.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-106">When you deploy the Lync Server 2013 mobility feature, you can use the new URLs that are available with the Microsoft Lync Server 2013 Autodiscover Service, or you can use your existing Web Services URLs.</span></span> <span data-ttu-id="0fc5f-107">Se você usar suas URLs existentes, os usuários precisarão inserir manualmente as URLs nas configurações do dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-107">If you use your existing URLs, users need to manually enter the URLs in their mobile device settings.</span></span> <span data-ttu-id="0fc5f-108">Essa opção geralmente é usada para solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-108">This option is typically used for troubleshooting.</span></span> <span data-ttu-id="0fc5f-109">Quando você usa as novas URLs, os clientes móveis podem descobrir automaticamente os recursos do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-109">When you use the new URLs, mobile clients can automatically discover Lync Server 2013 resources.</span></span> <span data-ttu-id="0fc5f-110">Ao oferecer suporte à descoberta automática, você precisa adicionar novos registros de sistema de nome de domínio (DNS).</span><span class="sxs-lookup"><span data-stu-id="0fc5f-110">When you support automatic discovery, you need to add new Domain Name System (DNS) records.</span></span> <span data-ttu-id="0fc5f-111">Esta seção descreve os registros DNS necessários para a descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-111">This section describes the DNS records that are required for automatic discovery.</span></span>

<span data-ttu-id="0fc5f-112">Para dar suporte à descoberta automática, você precisa criar os seguintes registros DNS para cada domínio SIP:</span><span class="sxs-lookup"><span data-stu-id="0fc5f-112">To support automatic discovery, you need to create the following DNS records for each SIP domain:</span></span>

  - <span data-ttu-id="0fc5f-113">Um registro DNS interno para dar suporte a usuários móveis que se conectam dentro da rede da sua organização</span><span class="sxs-lookup"><span data-stu-id="0fc5f-113">An internal DNS record to support mobile users who connect from within your organization's network</span></span>

  - <span data-ttu-id="0fc5f-114">Um registro DNS externo ou público para dar suporte a usuários móveis que se conectam à Internet</span><span class="sxs-lookup"><span data-stu-id="0fc5f-114">An external, or public, DNS record to support mobile users who connect from the Internet</span></span>

<span data-ttu-id="0fc5f-115">A URL de descoberta automática interna não deve ser endereçável de fora da rede.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-115">The internal automatic discovery URL should not be addressable from outside your network.</span></span> <span data-ttu-id="0fc5f-116">A URL de descoberta automática externa não deve ser endereçada dentro da sua rede.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-116">The external automatic discovery URL should not be addressable from within your network.</span></span> <span data-ttu-id="0fc5f-117">No entanto, se você não puder atender a esse requisito para a URL externa, a funcionalidade do cliente móvel não deve ser afetada.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-117">However, if you cannot meet this requirement for the external URL, mobile client functionally should not be affected.</span></span>

<span data-ttu-id="0fc5f-118">Os registros DNS podem ser registros CNAME ou registros (host).</span><span class="sxs-lookup"><span data-stu-id="0fc5f-118">The DNS records can be either CNAME records or A (host) records.</span></span>

<span data-ttu-id="0fc5f-119">**Registros DNS internos**</span><span class="sxs-lookup"><span data-stu-id="0fc5f-119">**Internal DNS records**</span></span>

<span data-ttu-id="0fc5f-120">Você precisa criar um dos seguintes registros de DNS interno:</span><span class="sxs-lookup"><span data-stu-id="0fc5f-120">You need to create one of the following internal DNS records:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0fc5f-121">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="0fc5f-121">Record type</span></span></th>
<th><span data-ttu-id="0fc5f-122">Nome do host ou definição de SRV</span><span class="sxs-lookup"><span data-stu-id="0fc5f-122">Host name or SRV definition</span></span></th>
<th><span data-ttu-id="0fc5f-123">Resolve para</span><span class="sxs-lookup"><span data-stu-id="0fc5f-123">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fc5f-124">CNAME</span><span class="sxs-lookup"><span data-stu-id="0fc5f-124">CNAME</span></span></p></td>
<td><p><span data-ttu-id="0fc5f-125">lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="0fc5f-125">lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="0fc5f-126">FQDN (nome de domínio totalmente qualificado) dos serviços Web internos para o seu pool de directors, se você tiver um ou para o seu pool de front-end se não tiver um director</span><span class="sxs-lookup"><span data-stu-id="0fc5f-126">Internal Web Services fully qualified domain name (FQDN) for your Director pool, if you have one, or for your Front End pool if you do not have a Director</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fc5f-127">A (host)</span><span class="sxs-lookup"><span data-stu-id="0fc5f-127">A (host)</span></span></p></td>
<td><p><span data-ttu-id="0fc5f-128">lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="0fc5f-128">lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="0fc5f-129">Endereço IP interno dos serviços Web (VIP) se você usar um balanceador de carga) do seu pool de director, se você tiver um ou do seu pool Front-End se não tiver um director</span><span class="sxs-lookup"><span data-stu-id="0fc5f-129">Internal Web Services IP address (virtual IP (VIP) address if you use a load balancer) of your Director pool, if you have one, or of your Front End pool if you do not have a Director</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0fc5f-130">**Registros DNS externos**</span><span class="sxs-lookup"><span data-stu-id="0fc5f-130">**External DNS records**</span></span>

<span data-ttu-id="0fc5f-131">Você precisa criar um dos seguintes registros de DNS externo:</span><span class="sxs-lookup"><span data-stu-id="0fc5f-131">You need to create one of the following external DNS records:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0fc5f-132">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="0fc5f-132">Record type</span></span></th>
<th><span data-ttu-id="0fc5f-133">Nome do host</span><span class="sxs-lookup"><span data-stu-id="0fc5f-133">Host name</span></span></th>
<th><span data-ttu-id="0fc5f-134">Resolve para</span><span class="sxs-lookup"><span data-stu-id="0fc5f-134">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fc5f-135">CNAME</span><span class="sxs-lookup"><span data-stu-id="0fc5f-135">CNAME</span></span></p></td>
<td><p><span data-ttu-id="0fc5f-136">lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-136">lyncdiscover.</span></span> <span data-ttu-id="0fc5f-137">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="0fc5f-137">&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="0fc5f-138">FQDN de serviços Web externos para o seu pool de directors, se você tiver um ou para o seu pool de front-end se não tiver um director</span><span class="sxs-lookup"><span data-stu-id="0fc5f-138">External Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fc5f-139">A (host)</span><span class="sxs-lookup"><span data-stu-id="0fc5f-139">A (host)</span></span></p></td>
<td><p><span data-ttu-id="0fc5f-140">lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-140">lyncdiscover.</span></span> <span data-ttu-id="0fc5f-141">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="0fc5f-141">&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="0fc5f-142">Endereço IP externo ou público (endereço VIP se você usar um balanceador de carga) do proxy reverso</span><span class="sxs-lookup"><span data-stu-id="0fc5f-142">External or public IP address (VIP address if you use a load balancer) of the reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fc5f-143">SRV</span><span class="sxs-lookup"><span data-stu-id="0fc5f-143">SRV</span></span></p></td>
<td><p><span data-ttu-id="0fc5f-144">_sipfederationtls._tcp.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-144">_sipfederationtls._tcp.</span></span> <span data-ttu-id="0fc5f-145">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="0fc5f-145">&lt;sipdomain&gt;</span></span></p>
<p><span data-ttu-id="0fc5f-146">Resolve para registro de host (A ou AAAA) do serviço de borda de acesso</span><span class="sxs-lookup"><span data-stu-id="0fc5f-146">Resolves to host (A or AAAA) record for the Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="0fc5f-147">Para dar suporte ao serviço de notificação por push e ao Apple Push Notification Service, crie um registro SRV para cada domínio SIP que tenha clientes móveis do Microsoft Lync.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-147">To support Push Notification Service and Apple Push Notification service, you create one SRV record for each SIP domain that has Microsoft Lync Mobile clients.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="0fc5f-148">Este requisito aplica-se somente aos clientes móveis do Microsoft Lync em dispositivos móveis baseados em Apple ou Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-148">This requirement applies only to Microsoft Lync Mobile clients on Apple or Microsoft based mobile devices.</span></span> <span data-ttu-id="0fc5f-149">Os dispositivos Android e Nokia Symbian não usam notificações por push.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-149">Andriod and Nokia Symbian devices do not use push notification.</span></span>


</div></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="0fc5f-150">Lyncdiscover, também conhecido como descoberta automática, o tráfego passa pelo proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-150">Lyncdiscover, also known as autodiscover, traffic goes through the reverse proxy.</span></span> <span data-ttu-id="0fc5f-151">O registro SRV aponta para um registro que é resolvido por meio do serviço de borda de acesso.</span><span class="sxs-lookup"><span data-stu-id="0fc5f-151">SRV record points to a record that resolves through the Access Edge service.</span></span>



<span data-ttu-id="0fc5f-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0fc5f-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

