---
title: 'Lync Server 2013: Resumo do certificado-conectividade de mensagens instantâneas públicas'
description: 'Lync Server 2013: Resumo do certificado-conectividade pública de mensagens instantâneas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Public instant messaging connectivity
ms:assetid: 2b3687ee-50c2-4c1c-880e-8dcf8bd4f309
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618370(v=OCS.15)
ms:contentKeyID: 49105657
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: abf5a01bdeb03da158e221c623417a1b42cc82f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435289"
---
# <a name="certificate-summary---public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="53ddb-103">Resumo do certificado-conectividade de mensagens instantâneas públicas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53ddb-103">Certificate summary - Public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="53ddb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="53ddb-104">

<span> </span></span></span>

<span data-ttu-id="53ddb-105">_**Tópico da última modificação:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="53ddb-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="53ddb-106">Para configurar certificados para a conectividade de mensagens instantâneas públicas, primeiro você deve observar que não há nada diferente de outros tipos de Federação SIP ou mesmo dos certificados de servidor de borda padrão, exceto que o America Online (AOL) requer uma configuração de certificado exclusiva.</span><span class="sxs-lookup"><span data-stu-id="53ddb-106">To configure certificates for public Instant Messaging connectivity, you should first notice that there is nothing different from other SIP federation types or even standard Edge Server certificates, except that America Online (AOL) requires a unique certificate configuration.</span></span> <span data-ttu-id="53ddb-107">Além do uso de chave avançada (EKU) do servidor usual, a America Online exige que o certificado ou certificados (no caso de um pool de bordas) também contenham o EKU do cliente.</span><span class="sxs-lookup"><span data-stu-id="53ddb-107">In addition to the usual server enhanced key usage (EKU), America Online requires the certificate or certificates (in the case of an Edge pool) to also contain the client EKU.</span></span> <span data-ttu-id="53ddb-108">O EKU do cliente é uma adição ao certificado e faz parte do certificado público externo atribuído ao seu servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="53ddb-108">The client EKU is an addition to the certificate, and is part of the external public certificate that is assigned to your Edge Server.</span></span>

<div>

## <a name="certificate-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="53ddb-109">Resumo do certificado – conectividade de mensagens instantâneas públicas</span><span class="sxs-lookup"><span data-stu-id="53ddb-109">Certificate Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53ddb-110">Componente</span><span class="sxs-lookup"><span data-stu-id="53ddb-110">Component</span></span></th>
<th><span data-ttu-id="53ddb-111">Nome do assunto</span><span class="sxs-lookup"><span data-stu-id="53ddb-111">Subject name</span></span></th>
<th><span data-ttu-id="53ddb-112">Nomes alternativos de assunto (SAN)/Order</span><span class="sxs-lookup"><span data-stu-id="53ddb-112">Subject alternative names (SAN)/Order</span></span></th>
<th><span data-ttu-id="53ddb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="53ddb-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53ddb-114">Borda externa/de acesso</span><span class="sxs-lookup"><span data-stu-id="53ddb-114">External/Access Edge</span></span></p></td>
<td><p><span data-ttu-id="53ddb-115">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="53ddb-115">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="53ddb-116">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="53ddb-116">sip.contoso.com</span></span></p>
<p><span data-ttu-id="53ddb-117">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="53ddb-117">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="53ddb-118">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="53ddb-118">sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="53ddb-119">O certificado deve ser de uma CA pública e deve ter o EKU do servidor e o cliente EKU se a conectividade de IM pública com AOL for implantada.</span><span class="sxs-lookup"><span data-stu-id="53ddb-119">The certificate must be from a Public CA, and must have the server EKU and client EKU if public IM connectivity with AOL is to be deployed.</span></span> <span data-ttu-id="53ddb-120">O certificado é atribuído às interfaces do servidor de borda externo para:</span><span class="sxs-lookup"><span data-stu-id="53ddb-120">The certificate is assigned to the external Edge Server interfaces for:</span></span></p>
<ul>
<li><p><span data-ttu-id="53ddb-121">Serviço de Borda de Acesso</span><span class="sxs-lookup"><span data-stu-id="53ddb-121">Access Edge service</span></span></p></li>
<li><p><span data-ttu-id="53ddb-122">Serviço de Borda de Webconferência</span><span class="sxs-lookup"><span data-stu-id="53ddb-122">Web Conferencing Edge service</span></span></p></li>
<li><p><span data-ttu-id="53ddb-123">Serviço de Borda A/V</span><span class="sxs-lookup"><span data-stu-id="53ddb-123">A/V Edge service</span></span></p></li>
</ul>
<p><span data-ttu-id="53ddb-124">Observe que as SANs são adicionadas automaticamente ao certificado com base em suas definições no construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="53ddb-124">Note that SANs are automatically added to the certificate based on your definitions in Topology Builder.</span></span> <span data-ttu-id="53ddb-125">Você adiciona entradas de SAN conforme necessário para domínios SIP adicionais e outras entradas de que você precisa para dar suporte.</span><span class="sxs-lookup"><span data-stu-id="53ddb-125">You add SAN entries as needed for additional SIP domains and other entries that you need to support.</span></span> <span data-ttu-id="53ddb-126">O nome do requerente é replicado na SAN e deve estar presente para a operação correta.</span><span class="sxs-lookup"><span data-stu-id="53ddb-126">The subject name is replicated in the SAN and must be present for correct operation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="53ddb-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="53ddb-127">See Also</span></span>


[<span data-ttu-id="53ddb-128">Cenários de acesso de usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53ddb-128">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
  

<span data-ttu-id="53ddb-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="53ddb-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

