---
title: 'Lync Server 2013: requisitos de infraestrutura de certificado'
description: Requisitos de infraestrutura de certificado do Lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate infrastructure requirements
ms:assetid: 0051aa23-0bbe-4e72-9f29-e01c6bcc6190
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398066(v=OCS.15)
ms:contentKeyID: 48183219
ms.date: 06/23/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02c7e69f272c29f0ba9386f403db326b4d39bbff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435408"
---
# <a name="certificate-infrastructure-requirements-for-lync-server-2013"></a><span data-ttu-id="71a5f-103">Requisitos de infraestrutura de certificado para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71a5f-103">Certificate infrastructure requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71a5f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71a5f-104">

<span> </span></span></span>

<span data-ttu-id="71a5f-105">_**Tópico da última modificação:** 2016-06-23_</span><span class="sxs-lookup"><span data-stu-id="71a5f-105">_**Topic Last Modified:** 2016-06-23_</span></span>

<span data-ttu-id="71a5f-106">O Lync Server 2013 requer uma infraestrutura de chave pública (PKI) para dar suporte a conexões TLS e TLS mútua (MTLS).</span><span class="sxs-lookup"><span data-stu-id="71a5f-106">Lync Server 2013 requires a public key infrastructure (PKI) to support TLS and mutual TLS (MTLS) connections.</span></span>

<span data-ttu-id="71a5f-107">O Lync Server usa certificados para as seguintes finalidades:</span><span class="sxs-lookup"><span data-stu-id="71a5f-107">Lync Server uses certificates for the following purposes:</span></span>

  - <span data-ttu-id="71a5f-108">Conexões de TLS entre cliente e servidor</span><span class="sxs-lookup"><span data-stu-id="71a5f-108">TLS connections between client and server</span></span>

  - <span data-ttu-id="71a5f-109">Conexões MTLS entre servidores</span><span class="sxs-lookup"><span data-stu-id="71a5f-109">MTLS connections between servers</span></span>

  - <span data-ttu-id="71a5f-110">Federação usando descoberta automática de DNS de parceiros</span><span class="sxs-lookup"><span data-stu-id="71a5f-110">Federation using automatic DNS discovery of partners</span></span>

  - <span data-ttu-id="71a5f-111">Acesso de usuários remotos a IM (mensagens instantâneas)</span><span class="sxs-lookup"><span data-stu-id="71a5f-111">Remote user access for instant messaging (IM)</span></span>

  - <span data-ttu-id="71a5f-112">Acesso de usuário externo a sessões de áudio/vídeo (A/V), compartilhamento de aplicativos e conferência</span><span class="sxs-lookup"><span data-stu-id="71a5f-112">External user access to audio/video (A/V) sessions, application sharing, and conferencing</span></span>

  - <span data-ttu-id="71a5f-113">Solicitações móveis usando a descoberta automática de serviços Web</span><span class="sxs-lookup"><span data-stu-id="71a5f-113">Mobile requests using automatic discovery of Web Services</span></span>

<span data-ttu-id="71a5f-114">Para o Lync Server, os seguintes requisitos comuns se aplicam:</span><span class="sxs-lookup"><span data-stu-id="71a5f-114">For Lync Server, the following common requirements apply:</span></span>

  - <span data-ttu-id="71a5f-115">Todos os certificados de servidor devem oferecer suporte à autorização de servidor (EKU de servidor).</span><span class="sxs-lookup"><span data-stu-id="71a5f-115">All server certificates must support server authorization (Server EKU).</span></span>

  - <span data-ttu-id="71a5f-116">Todos os certificados de servidor devem conter um CDP (Ponto de Distribuição de CRL).</span><span class="sxs-lookup"><span data-stu-id="71a5f-116">All server certificates must contain a CRL Distribution Point (CDP).</span></span>

  - <span data-ttu-id="71a5f-117">Todos os certificados devem ser assinados usando um algoritmo de assinatura que seja compatível com o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="71a5f-117">All certificates must be signed using a signing algorithm supported by the operating system.</span></span> <span data-ttu-id="71a5f-118">O Lync Server 2013 é compatível com o pacote de Resumo de SHA-1 e SHA-2 (224, 256, 384 e 512) e atende ou supera os requisitos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="71a5f-118">Lync Server 2013 supports the SHA-1 and SHA-2 suite of digest sizes (224, 256, 384 and 512-bit), and meets or exceeds the operating system requirements.</span></span> <span data-ttu-id="71a5f-119">Para obter suporte para o sistema operacional, consulte [https://go.microsoft.com/fwlink/?LinkId=287002](https://go.microsoft.com/fwlink/?linkid=287002) .</span><span class="sxs-lookup"><span data-stu-id="71a5f-119">For operating system support, see [https://go.microsoft.com/fwlink/?LinkId=287002](https://go.microsoft.com/fwlink/?linkid=287002).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="71a5f-120">O uso do algoritmo de assinatura RSASSA-PSS não é permitido e pode levar a erros no login e a problemas de encaminhamento de chamadas, entre outros. </span><span class="sxs-lookup"><span data-stu-id="71a5f-120">Using the RSASSA-PSS signature algorithm is unsupported, and may lead to errors on login and call forwarding issues, among other problems.</span></span>

    
    </div>

  - <span data-ttu-id="71a5f-121">O registro automático tem suporte para servidores internos que executam o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="71a5f-121">Auto-enrollment is supported for internal servers running Lync Server.</span></span>

  - <span data-ttu-id="71a5f-122">Não há suporte para a inscrição automática nos servidores do Lync Server Edge.</span><span class="sxs-lookup"><span data-stu-id="71a5f-122">Auto-enrollment is not supported for Lync Server Edge Servers.</span></span>

  - <span data-ttu-id="71a5f-123">Ao enviar uma solicitação de certificado baseada na Web para uma autoridade de certificação do Windows Server 2003, você deve enviá-la a partir de um computador que esteja executando o Windows Server 2003 com SP2 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="71a5f-123">When you submit a web-based certificate request to a Windows Server 2003 CA, you must submit it from a computer running either Windows Server 2003 with SP2 or Windows XP.</span></span>
    
    <span data-ttu-id="71a5f-124">Observe que, embora o KB922706 forneça suporte para resolver problemas com a inscrição de certificados da Web em relação a um registro na Web de serviços de certificado do Windows Server 2003, ele não permite usar o Windows Server 2008, o Windows Vista ou o Windows 7 para solicitar um certificado de uma autoridade de certificação do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="71a5f-124">Note that although KB922706 provides support for resolving issues with enrolling web certificates against a Windows Server 2003 Certificate Services web enrollment, it does not make it possible to use Windows Server 2008, Windows Vista, or Windows 7 to request a certificate from a Windows Server 2003 CA.</span></span>

  - <span data-ttu-id="71a5f-125">Os comprimentos de chave de criptografia de 1024, 2048 e 4096 são suportados.</span><span class="sxs-lookup"><span data-stu-id="71a5f-125">Encryption key lengths of 1024, 2048, and 4096 are supported.</span></span> <span data-ttu-id="71a5f-126">Comprimentos de pelo menos 2048 são recomendados.</span><span class="sxs-lookup"><span data-stu-id="71a5f-126">Key lengths of 2048 and greater are recommended.</span></span>

  - <span data-ttu-id="71a5f-127">O algoritmo de hash de assinatura ou sumário padrão é RSA.</span><span class="sxs-lookup"><span data-stu-id="71a5f-127">The default digest, or hash signing, algorithm is RSA.</span></span> <span data-ttu-id="71a5f-128">Os \_ algoritmos ECDH P256, ECDH \_ P384 e ECDH \_ P521 também têm suporte.</span><span class="sxs-lookup"><span data-stu-id="71a5f-128">The ECDH\_P256, ECDH\_P384, and ECDH\_P521 algorithms are also supported.</span></span> 

<div>

## <a name="in-this-section"></a><span data-ttu-id="71a5f-129">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="71a5f-129">In This Section</span></span>

  - [<span data-ttu-id="71a5f-130">Requisitos de certificado para servidores internos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71a5f-130">Certificate requirements for internal servers in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [<span data-ttu-id="71a5f-131">Requisitos de certificado para acesso do usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71a5f-131">Certificate requirements for external user access in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [<span data-ttu-id="71a5f-132">Requisitos de certificado para o servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71a5f-132">Certificate requirements for Persistent Chat server in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="71a5f-133">Requisitos de certificado para mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71a5f-133">Certificate requirements for mobility in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-mobility.md)

<span data-ttu-id="71a5f-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71a5f-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

