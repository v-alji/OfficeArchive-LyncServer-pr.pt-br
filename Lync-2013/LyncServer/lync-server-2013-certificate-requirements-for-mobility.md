---
title: 'Lync Server 2013: Requisitos de certificado para mobilidade'
description: 'Lync Server 2013: requisitos de certificado para mobilidade.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for mobility
ms:assetid: bb0e97af-cf60-4271-a0ab-654429d884ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690044(v=OCS.15)
ms:contentKeyID: 48185251
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 51af74b3efc1ffcb4fe38d7431e315f9b55af943
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435359"
---
# <a name="certificate-requirements-for-mobility-in-lync-server-2013"></a><span data-ttu-id="9cced-103">Requisitos de certificado para mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9cced-103">Certificate requirements for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9cced-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9cced-104">

<span> </span></span></span>

<span data-ttu-id="9cced-105">_**Tópico da última modificação:** 2012-06-24_</span><span class="sxs-lookup"><span data-stu-id="9cced-105">_**Topic Last Modified:** 2012-06-24_</span></span>

<span data-ttu-id="9cced-106">Se você implantar o recurso de mobilidade e oferecer suporte à descoberta automática para clientes móveis, será necessário incluir certas entradas de nomes alternativos de entidades nos certificados para dar suporte a conexões seguras de clientes móveis.</span><span class="sxs-lookup"><span data-stu-id="9cced-106">If you deploy the mobility feature and support automatic discovery for mobile clients, you need to include certain subject alternative name entries on certificates to support secure connections from the mobile clients.</span></span>

<span data-ttu-id="9cced-107">Você precisa incluir entradas de nomes alternativos de entidades para descoberta automática nos seguintes certificados:</span><span class="sxs-lookup"><span data-stu-id="9cced-107">You need to include subject alternative name entries for automatic discovery on the following certificates:</span></span>

  - <span data-ttu-id="9cced-108">Pool de diretores</span><span class="sxs-lookup"><span data-stu-id="9cced-108">Director pool</span></span>

  - <span data-ttu-id="9cced-109">Pool de Front-Ends</span><span class="sxs-lookup"><span data-stu-id="9cced-109">Front End pool</span></span>

  - <span data-ttu-id="9cced-110">Proxy reverso</span><span class="sxs-lookup"><span data-stu-id="9cced-110">Reverse proxy</span></span>

<span data-ttu-id="9cced-111">Esta seção descreve as entradas de nome alternativo do assunto que são necessárias em seus certificados para descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="9cced-111">This section describes the subject alternative name entries that are required on your certificates for automatic discovery.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9cced-112">A emissão de certificados por meio de uma autoridade de certificação interna geralmente é um processo simples, mas adicionar várias entradas de nome alternativo à entidade para certificados públicos usados pelo proxy reverso pode ser caro.</span><span class="sxs-lookup"><span data-stu-id="9cced-112">Reissuing certificates by using an internal certificate authority is typically a simple process, but adding multiple subject alternative name entries to public certificates used by the reverse proxy can be expensive.</span></span> <span data-ttu-id="9cced-113">Se você tiver muitos domínios SIP, o que faz com que a adição dos nomes alternativos de assunto seja muito cara, você pode configurar o proxy reverso para usar HTTP para a solicitação inicial de serviço de descoberta automática, em vez de usar HTTPS (a configuração padrão).</span><span class="sxs-lookup"><span data-stu-id="9cced-113">If you have many SIP domains, making the addition of subject alternative names very expensive, you can configure the reverse proxy to use HTTP for the initial Autodiscover Service request, instead of using HTTPS (the default configuration).</span></span> <span data-ttu-id="9cced-114">Para obter detalhes, consulte <A href="lync-server-2013-technical-requirements-for-mobility.md">requisitos técnicos de mobilidade no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9cced-114">For details, see <A href="lync-server-2013-technical-requirements-for-mobility.md">Technical requirements for mobility in Lync Server 2013</A>.</span></span>



</div>

### <a name="director-pool-certificate-requirements"></a><span data-ttu-id="9cced-115">Requisitos de certificado do pool do director</span><span class="sxs-lookup"><span data-stu-id="9cced-115">Director Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9cced-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9cced-116">Description</span></span></th>
<th><span data-ttu-id="9cced-117">Entrada de nome alternativo do assunto</span><span class="sxs-lookup"><span data-stu-id="9cced-117">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9cced-118">URL interna do serviço de descoberta automática</span><span class="sxs-lookup"><span data-stu-id="9cced-118">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="9cced-119">SAN = lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="9cced-119">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9cced-120">URL do serviço de descoberta automática externo</span><span class="sxs-lookup"><span data-stu-id="9cced-120">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="9cced-121">SAN = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="9cced-121">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="9cced-122">Você também pode usar SAN = \*. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="9cced-122">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="front-end-pool-certificate-requirements"></a><span data-ttu-id="9cced-123">Requisitos de certificado de pool de front-end</span><span class="sxs-lookup"><span data-stu-id="9cced-123">Front End Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9cced-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="9cced-124">Description</span></span></th>
<th><span data-ttu-id="9cced-125">Entrada de nome alternativo do assunto</span><span class="sxs-lookup"><span data-stu-id="9cced-125">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9cced-126">URL interna do serviço de descoberta automática</span><span class="sxs-lookup"><span data-stu-id="9cced-126">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="9cced-127">SAN = lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="9cced-127">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9cced-128">URL do serviço de descoberta automática externo</span><span class="sxs-lookup"><span data-stu-id="9cced-128">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="9cced-129">SAN = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="9cced-129">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="9cced-130">Você também pode usar SAN = \*. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="9cced-130">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="reverse-proxy-public-ca-certificate-requirements"></a><span data-ttu-id="9cced-131">Requisitos de certificado de proxy reverso (CA pública)</span><span class="sxs-lookup"><span data-stu-id="9cced-131">Reverse Proxy (Public CA) Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9cced-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="9cced-132">Description</span></span></th>
<th><span data-ttu-id="9cced-133">Entrada de nome alternativo do assunto</span><span class="sxs-lookup"><span data-stu-id="9cced-133">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9cced-134">URL do serviço de descoberta automática externo</span><span class="sxs-lookup"><span data-stu-id="9cced-134">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="9cced-135">SAN = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="9cced-135">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="9cced-136">Você atribui esta SAN ao certificado atribuído ao ouvinte SSL no proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="9cced-136">You assign this SAN to the certificate assigned to the SSL Listener on the reverse proxy.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="9cced-137">Seu ouvinte de proxy reverso terá nomes alternativos de entidades para seus serviços Web externos (por exemplo, SAN = lyncwebextpool01. contoso. com e dirwebexternal.contoso.com se você tiver implantado o diretor opcional).</span><span class="sxs-lookup"><span data-stu-id="9cced-137">Your reverse proxy listener will have subject alternative names for your external Web Services URL(s) (for example, SAN=lyncwebextpool01.contoso.com, and dirwebexternal.contoso.com if you have deployed the optional Director).</span></span>



<span data-ttu-id="9cced-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9cced-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

