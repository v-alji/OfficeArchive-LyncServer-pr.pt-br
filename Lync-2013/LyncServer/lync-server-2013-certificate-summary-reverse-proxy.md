---
title: 'Lync Server 2013: Resumo de certificado - Proxy reverso'
description: 'Lync Server 2013: Resumo do certificado-proxy reverso.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Reverse proxy
ms:assetid: f2b9a53f-aead-413d-81e9-4a294a010fbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205381(v=OCS.15)
ms:contentKeyID: 48185820
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0cc250d6de2eb1a0b6c3ad3495c8df62942f9a81
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435269"
---
# <a name="certificate-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="f6ecb-103">Resumo de certificado - Proxy reverso no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f6ecb-103">Certificate summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f6ecb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f6ecb-104">

<span> </span></span></span>

<span data-ttu-id="f6ecb-105">_**Tópico da última modificação:** 2012-11-14_</span><span class="sxs-lookup"><span data-stu-id="f6ecb-105">_**Topic Last Modified:** 2012-11-14_</span></span>

<span data-ttu-id="f6ecb-106">Os requisitos de certificado para o proxy reverso são muito mais simples do que os servidores de borda.</span><span class="sxs-lookup"><span data-stu-id="f6ecb-106">Certificate requirements for the reverse proxy are much simpler than that for the Edge Servers.</span></span> <span data-ttu-id="f6ecb-107">O fluxograma fornecido apresenta os requisitos necessários.</span><span class="sxs-lookup"><span data-stu-id="f6ecb-107">The provided flowchart presents the requirements necessary.</span></span> <span data-ttu-id="f6ecb-108">A tabela a seguir apresenta nomes de entidades de certificado típicos e nomes alternativos de assunto em relação aos cenários em que foi revisado nas discussões do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="f6ecb-108">The accompanying table presents typical certificate subject name and subject alternative names in relation to the scenarios that we have been reviewed in the Edge Server discussions.</span></span> <span data-ttu-id="f6ecb-109">Para obter mais detalhes sobre os cenários do servidor de borda, consulte [cenários para acesso de usuários externos no Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="f6ecb-109">For more details on the Edge Server scenarios, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

<span data-ttu-id="f6ecb-110">**Fluxograma de certificados para proxy reverso**</span><span class="sxs-lookup"><span data-stu-id="f6ecb-110">**Certificates Flow Chart for Reverse Proxy**</span></span>

<span data-ttu-id="f6ecb-111">![Fluxograma de certificados do servidor de borda](images/JJ205381.026045d7-1b4b-4651-b32f-2d43a7161198(OCS.15).jpg "Fluxograma de certificados do servidor de borda")</span><span class="sxs-lookup"><span data-stu-id="f6ecb-111">![Certificates Flow Chart for Edge Server](images/JJ205381.026045d7-1b4b-4651-b32f-2d43a7161198(OCS.15).jpg "Certificates Flow Chart for Edge Server")</span></span>

### <a name="reverse-proxy-external-interface"></a><span data-ttu-id="f6ecb-112">Proxy inverso: interface externa</span><span class="sxs-lookup"><span data-stu-id="f6ecb-112">Reverse Proxy: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6ecb-113">Componente</span><span class="sxs-lookup"><span data-stu-id="f6ecb-113">Component</span></span></th>
<th><span data-ttu-id="f6ecb-114">Nome do assunto</span><span class="sxs-lookup"><span data-stu-id="f6ecb-114">Subject name</span></span></th>
<th><span data-ttu-id="f6ecb-115">Nome alternativo do assunto (SAN)/Order</span><span class="sxs-lookup"><span data-stu-id="f6ecb-115">Subject alternative name (SAN)/Order</span></span></th>
<th><span data-ttu-id="f6ecb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6ecb-116">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6ecb-117">Proxy reverso</span><span class="sxs-lookup"><span data-stu-id="f6ecb-117">Reverse Proxy</span></span></p></td>
<td><p><span data-ttu-id="f6ecb-118">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f6ecb-118">webext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f6ecb-119">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f6ecb-119">webext.contoso.com</span></span></p>
<p><span data-ttu-id="f6ecb-120">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f6ecb-120">webdirext.contoso.com</span></span></p>
<p><span data-ttu-id="f6ecb-121">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f6ecb-121">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="f6ecb-122">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f6ecb-122">meet.contoso.com</span></span></p>
<p><span data-ttu-id="f6ecb-123">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f6ecb-123">officewebapps01.contoso.com</span></span></p>
<p><span data-ttu-id="f6ecb-124">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f6ecb-124">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="f6ecb-125">(Opcional):\*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="f6ecb-125">(Optional):\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f6ecb-126">O certificado deve ser emitido por uma CA pública e com o EKU do servidor.</span><span class="sxs-lookup"><span data-stu-id="f6ecb-126">Certificate must be issued by a public CA and with the server EKU.</span></span> <span data-ttu-id="f6ecb-127">Serviços incluem serviço de catálogo de endereços, expansão do grupo de distribuição Office Web Apps para conferência e regras de publicação de dispositivo IP do Lync.</span><span class="sxs-lookup"><span data-stu-id="f6ecb-127">Services include Address Book Service, distribution group expansion Office Web Apps for conferencing, and Lync IP Device publishing rules.</span></span> <span data-ttu-id="f6ecb-128">O nome alternativo para o assunto inclui:</span><span class="sxs-lookup"><span data-stu-id="f6ecb-128">Subject alternative name includes:</span></span></p>
<ul>
<li><p><span data-ttu-id="f6ecb-129">FQDN de serviços Web externos para servidor front-end ou pool de front-end</span><span class="sxs-lookup"><span data-stu-id="f6ecb-129">External Web Services FQDN for Front End Server or Front End pool</span></span></p></li>
<li><p><span data-ttu-id="f6ecb-130">FQDN de serviços Web externos para o diretor ou pool do diretor</span><span class="sxs-lookup"><span data-stu-id="f6ecb-130">External Web Services FQDN for Director or Director pool</span></span></p></li>
<li><p><span data-ttu-id="f6ecb-131">Conferência discada</span><span class="sxs-lookup"><span data-stu-id="f6ecb-131">Dial-in conferencing</span></span></p></li>
<li><p><span data-ttu-id="f6ecb-132">Regra de publicação de reunião online</span><span class="sxs-lookup"><span data-stu-id="f6ecb-132">Online meeting publishing rule</span></span></p></li>
<li><p><span data-ttu-id="f6ecb-133">Office Web Apps para conferência</span><span class="sxs-lookup"><span data-stu-id="f6ecb-133">Office Web Apps for conferencing</span></span></p></li>
<li><p><span data-ttu-id="f6ecb-134">Lyncdiscover (descoberta automática)</span><span class="sxs-lookup"><span data-stu-id="f6ecb-134">Lyncdiscover (Autodiscover)</span></span></p></li>
</ul>
<p><span data-ttu-id="f6ecb-135">O curinga opcional substitui a SAN e a discagem</span><span class="sxs-lookup"><span data-stu-id="f6ecb-135">The optional wildcard replaces both meet and dialin SAN</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f6ecb-136">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f6ecb-136">


</div>

<span> </span>

</div>

</div>

</span></span></div>

