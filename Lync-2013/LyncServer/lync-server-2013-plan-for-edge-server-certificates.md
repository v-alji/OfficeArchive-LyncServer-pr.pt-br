---
title: 'Lync Server 2013: Planejar certificados do Servidor de Borda'
description: 'Lync Server 2013: planejar certificados de servidor de borda.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Plan for Edge Server certificates
ms:assetid: f1dfe220-2398-4ac8-ba4c-206c8c0cbc50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413010(v=OCS.15)
ms:contentKeyID: 48185798
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22ec3743256fe3e4c55dba0f6357a85b1ad81cd0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437124"
---
# <a name="plan-for-edge-server-certificates-in-lync-server-2013"></a><span data-ttu-id="607f9-103">Planejar certificados do Servidor de Borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="607f9-103">Plan for Edge Server certificates in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="607f9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="607f9-104">

<span> </span></span></span>

<span data-ttu-id="607f9-105">_**Tópico da última modificação:** 2012-11-05_</span><span class="sxs-lookup"><span data-stu-id="607f9-105">_**Topic Last Modified:** 2012-11-05_</span></span>

<span data-ttu-id="607f9-106">A criação de certificados para o Edge é simplificada no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="607f9-106">Certificate creation for Edge is simplified in Lync Server 2013.</span></span>

<span data-ttu-id="607f9-107">**Fluxograma de certificados do servidor de borda**</span><span class="sxs-lookup"><span data-stu-id="607f9-107">**Certificates Flow Chart for Edge Server**</span></span>

<span data-ttu-id="607f9-108">![a5fc20db-7ced-4364-b577-6a709a8367cd](images/Gg413010.a5fc20db-7ced-4364-b577-6a709a8367cd(OCS.15).jpg "a5fc20db-7ced-4364-b577-6a709a8367cd")</span><span class="sxs-lookup"><span data-stu-id="607f9-108">![a5fc20db-7ced-4364-b577-6a709a8367cd](images/Gg413010.a5fc20db-7ced-4364-b577-6a709a8367cd(OCS.15).jpg "a5fc20db-7ced-4364-b577-6a709a8367cd")</span></span>

<span data-ttu-id="607f9-109">Crie um único certificado público, verifique se você tem uma chave privada exportável definida para o certificado e atribui-la às seguintes interfaces externas do servidor de borda usando o assistente de certificado:</span><span class="sxs-lookup"><span data-stu-id="607f9-109">Create a single public certificate, ensure that you have an exportable private key defined for the certificate, and assign it to the following Edge Server external interfaces using the certificate wizard:</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="607f9-110">Não há suporte para certificados curinga no Lync Server, exceto onde usados para resumir as URLs simples por meio do proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="607f9-110">Wildcard certificates are not supported in Lync Server, except where used to summarize the Simple URLs through the reverse proxy.</span></span> <span data-ttu-id="607f9-111">Você deve definir nomes alternativos de assunto distintos (SANs) para cada nome de domínio SIP, serviço de borda de webconferência, serviço de borda A/V e domínio XMPP oferecidos pela sua implantação.</span><span class="sxs-lookup"><span data-stu-id="607f9-111">You must define distinct subject alternate names (SANs) for each SIP domain name, Web Conferencing Edge service, A/V Edge service and XMPP domain offered by your deployment.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="607f9-112">Apresentado no Lync Server 2013, a transferência de certificados de autenticação de áudio/vídeo antes do tempo de expiração do certificado atual requer algum planejamento adicional.</span><span class="sxs-lookup"><span data-stu-id="607f9-112">Introduced in Lync Server 2013, staging Audio/Video Authentication certificates in advance of the expiration time of the current certificate requires some additional planning.</span></span> <span data-ttu-id="607f9-113">Em vez de um certificado com várias finalidades para a interface de borda externa, você precisará de dois certificados, um atribuído ao serviço de borda de acesso e serviço de borda de Webconferência e um certificado para o serviço de borda A/V.</span><span class="sxs-lookup"><span data-stu-id="607f9-113">Instead of one certificate with multiple purposes for the external Edge interface, you will require two certificates, one assigned to the Access Edge service and Web Conferencing Edge service, and one certificate for the A/V Edge service.</span></span> <span data-ttu-id="607f9-114">Para obter mais detalhes, consulte <A href="lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate">preparando certificados do AV e do OAuth no Lync Server 2013 usando o-roll Set-CsCertificate</A></span><span class="sxs-lookup"><span data-stu-id="607f9-114">For additional details, see <A href="lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate">Staging AV and OAuth certificates in Lync Server 2013 using -Roll in Set-CsCertificate</A></span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="607f9-115">No caso de um pool de servidores de borda, exporte o certificado com a chave particular para cada servidor de borda e atribua o certificado a cada serviço de servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="607f9-115">In the event of a pool of Edge Servers, you export the certificate with the private key to each Edge Server and assign the certificate to each Edge Server service.</span></span> <span data-ttu-id="607f9-116">Faça o mesmo para o certificado interno do servidor de borda, exportando o certificado com a chave privada e atribuindo a cada interface de borda interna.</span><span class="sxs-lookup"><span data-stu-id="607f9-116">Do the same for the internal Edge Server certificate, exporting the certificate with the private key and assigning to each internal Edge interface.</span></span>



</div>

  - <span data-ttu-id="607f9-117">Verifique se você tem uma chave privada exportável atribuída para o certificado</span><span class="sxs-lookup"><span data-stu-id="607f9-117">Ensure that you have an exportable private key assigned for the certificate</span></span>

  - <span data-ttu-id="607f9-118">Serviço de borda de acesso (chamado de **borda de acesso SIP externa** no assistente de certificado)</span><span class="sxs-lookup"><span data-stu-id="607f9-118">Access Edge service (referred to as **SIP Access Edge External** in the certificate wizard)</span></span>

  - <span data-ttu-id="607f9-119">Serviço de borda de Webconferência (chamado de **borda de Webconferência externa** no assistente de certificado)</span><span class="sxs-lookup"><span data-stu-id="607f9-119">Web Conferencing Edge service (referred to as **Web Conferencing Edge External** in the certificate wizard)</span></span>

  - <span data-ttu-id="607f9-120">Serviço de autenticação a/V (chamado de **borda de a/v externa** no assistente de certificado)</span><span class="sxs-lookup"><span data-stu-id="607f9-120">A/V Authentication service (referred to as **A/V Edge External** in the certificate wizard)</span></span>

<span data-ttu-id="607f9-121">Crie um único certificado interno com a chave privada exportável, copie e atribua-o a cada uma das interfaces internas do servidor de borda:</span><span class="sxs-lookup"><span data-stu-id="607f9-121">Create a single internal certificate with exportable private key, copy and assign it to each of the Edge Server internal interfaces:</span></span>

  - <span data-ttu-id="607f9-122">Servidor de borda (chamado de **borda interna** no assistente de certificado)</span><span class="sxs-lookup"><span data-stu-id="607f9-122">Edge Server (referred to as **Edge Internal** in the certificate wizard)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="607f9-123">É possível usar certificados separados e distintos para cada serviço do servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="607f9-123">It is possible to use separate and distinct certificates for each Edge Server service.</span></span> <span data-ttu-id="607f9-124">Um bom motivo para escolher certificados separados é se você quiser usar o novo recurso de certificado de reversão para o certificado de serviço de borda A/V.</span><span class="sxs-lookup"><span data-stu-id="607f9-124">A good reason to choose separate certificates is if you want to use the new rolling certificate feature for the A/V Edge service certificate.</span></span> <span data-ttu-id="607f9-125">No caso desse recurso, é recomendável a dissociação do certificado de serviço de borda a/V do serviço de borda de acesso e do serviço de borda de conferência via Web.</span><span class="sxs-lookup"><span data-stu-id="607f9-125">In the case of this feature, decoupling the A/V Edge service certificate from the Access Edge service and Web Conferencing Edge service is recommended.</span></span> <span data-ttu-id="607f9-126">Se você optar por solicitar, adquirir e atribuir certificados separados para cada serviço, será necessário solicitar que a chave privada seja exportável para o serviço de borda A/V (novamente, isso está em realidade, o serviço de autenticação A/V) e atribui o mesmo certificado à interface externa de Edge a/V em cada servidor de borda.</span><span class="sxs-lookup"><span data-stu-id="607f9-126">If you choose to request, acquire and assign separate certificates for each service, you must request that the private key be exportable for the A/V Edge service (again, this is in actuality the A/V Authentication service) and assign the same certificate to the A/V Edge External interface on each Edge Server.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="607f9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="607f9-127">See Also</span></span>


[<span data-ttu-id="607f9-128">Preparando certificados do AV e do OAuth no Lync Server 2013 usando-roll no set-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="607f9-128">Staging AV and OAuth certificates in Lync Server 2013 using -Roll in Set-CsCertificate</span></span>](lync-server-2013-staging-av-and-oauth-certificates-using-roll-in-https://docs.microsoft.com/powershell/module/skype/Set-CsCertificate)  


[<span data-ttu-id="607f9-129">Alterações no Lync Server 2013 que afetam o planejamento do Servidor de Borda</span><span class="sxs-lookup"><span data-stu-id="607f9-129">Changes in Lync Server 2013 that affect Edge Server planning</span></span>](lync-server-2013-changes-in-lync-server-that-affect-edge-server-planning.md)  
  

<span data-ttu-id="607f9-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="607f9-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

