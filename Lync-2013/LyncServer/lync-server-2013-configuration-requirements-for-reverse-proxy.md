---
title: 'Lync Server 2013: requisitos de configuração para proxy reverso'
description: 'Lync Server 2013: requisitos de configuração para proxy reverso.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration requirements for reverse proxy
ms:assetid: c37d688a-28e4-4822-80cc-6add59c71052
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945651(v=OCS.15)
ms:contentKeyID: 51541518
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 75f3f5b9437ba4518e3feffc193853b446b702d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390371"
---
# <a name="configuration-requirements-for-reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="a704a-103">Requisitos de configuração para o proxy inverso no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a704a-103">Configuration requirements for reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a704a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a704a-104">

<span> </span></span></span>

<span data-ttu-id="a704a-105">_**Tópico da última modificação:** 2013-03-05_</span><span class="sxs-lookup"><span data-stu-id="a704a-105">_**Topic Last Modified:** 2013-03-05_</span></span>

<span data-ttu-id="a704a-106">O Lync Server 2013 imponha alguns requisitos sobre comunicações do cliente externo que, em seguida, passaram para os serviços Web externos hospedados no director, pool do diretor, servidor front-end ou pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="a704a-106">Lync Server 2013 imposes a few requirements on communications from the external client that are then passed on to the external Web services hosted on the Director, Director pool, Front End Server or Front End pool.</span></span> <span data-ttu-id="a704a-107">O proxy inverso também é responsável por publicar o servidor do Office Web Apps, se você estiver oferecendo conferências para seus usuários.</span><span class="sxs-lookup"><span data-stu-id="a704a-107">The reverse proxy is also responsible for publishing the Office Web Apps Server, if you are offering conferencing to your users.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a704a-108">O Lync Server 2013 não especifica um determinado proxy reverso que você deve usar.</span><span class="sxs-lookup"><span data-stu-id="a704a-108">Lync Server 2013 does not specify a particular reverse proxy that you must use.</span></span> <span data-ttu-id="a704a-109">O Lync Server 2013 define somente requisitos operacionais que o proxy reverso deve ser capaz de fazer.</span><span class="sxs-lookup"><span data-stu-id="a704a-109">Lync Server 2013 only defines operational requirements that the reverse proxy must be able to do.</span></span> <span data-ttu-id="a704a-110">Geralmente, o proxy inverso que você já implantou na sua infraestrutura pode atender aos requisitos.</span><span class="sxs-lookup"><span data-stu-id="a704a-110">Typically, the reverse proxy that you already have deployed in your infrastructure may be able to meet the requirements.</span></span>



</div>

<div>

## <a name="reverse-proxy-requirements"></a><span data-ttu-id="a704a-111">Requisitos de proxy reverso</span><span class="sxs-lookup"><span data-stu-id="a704a-111">Reverse Proxy Requirements</span></span>

<span data-ttu-id="a704a-112">As operações funcionais que o Lync Server 2013 esperam que um proxy reverso execute:</span><span class="sxs-lookup"><span data-stu-id="a704a-112">The functional operations that Lync Server 2013 expect a reverse proxy to perform are:</span></span>

  - <span data-ttu-id="a704a-113">Use Secure Socket Layer (SSL) e Transport Layer Security (TLS) implementado usando certificados adquiridos de uma autoridade de certificação pública para se conectar aos serviços Web externos publicados do diretor, do pool de director, do servidor front-end ou do pool de front-ends.</span><span class="sxs-lookup"><span data-stu-id="a704a-113">Use secure socket layer (SSL) and transport layer security (TLS) implemented by using certificates acquired from a public certification authority to connect to the published external Web services of the Director, Director pool, Front End Server or Front End pool.</span></span> <span data-ttu-id="a704a-114">O diretor e o servidor front-end podem estar em um pool de balanceamento de carga usando balanceadores de carga de hardware.</span><span class="sxs-lookup"><span data-stu-id="a704a-114">The Director and the Front End Server can be in a load-balanced pool by using hardware load balancers.</span></span>

  - <span data-ttu-id="a704a-115">Pode publicar sites internos usando certificados para criptografia ou publicá-los por meio de um meio não criptografado, se necessário.</span><span class="sxs-lookup"><span data-stu-id="a704a-115">Able to publish internal Web sites using certificates for encryption, or publish them over an unencrypted means, if needed.</span></span>

  - <span data-ttu-id="a704a-116">Capaz de publicar um site da Web hospedado internamente externamente usando um FQDN (nome de domínio totalmente qualificado).</span><span class="sxs-lookup"><span data-stu-id="a704a-116">Able to publish an internally hosted web site externally by using a fully qualified domain name (FQDN).</span></span>

  - <span data-ttu-id="a704a-117">Pode publicar todo o conteúdo do site hospedado.</span><span class="sxs-lookup"><span data-stu-id="a704a-117">Able to publish all contents of the hosted web site.</span></span> <span data-ttu-id="a704a-118">Por padrão, você pode usar a **/ \* *diretiva _, que é reconhecida pela maioria dos servidores Web, para significar "publicar todo o conteúdo no servidor Web". Você também pode modificar a diretiva — por exemplo, _*/Uwca/ \***, que significa "publicar todo o conteúdo sob o diretório virtual Ucwa".</span><span class="sxs-lookup"><span data-stu-id="a704a-118">By default, you can use the **/\**_ directive, which is recognized by most web servers to mean "Publish all content on the web server." You can also modify the directive—for example, _*/Uwca/\***, which means "Publish all content under the virtual directory Ucwa."</span></span>

  - <span data-ttu-id="a704a-119">Deve ser configurável para exigir conexões SSL (Secure Sockets Layer) e/ou Transport Layer Security (TLS) com clientes que solicitam conteúdo de um site publicado.</span><span class="sxs-lookup"><span data-stu-id="a704a-119">Must be configurable to require Secure Sockets Layer (SSL) and/or Transport Layer Security (TLS) connections with clients that request content from a published website.</span></span>

  - <span data-ttu-id="a704a-120">Deve aceitar certificados com entradas de nome alternativo de assunto (SAN).</span><span class="sxs-lookup"><span data-stu-id="a704a-120">Must accept certificates with subject alternative name (SAN) entries.</span></span>

  - <span data-ttu-id="a704a-121">Deve ser capaz de permitir a associação de um certificado a um ouvinte ou interface por meio do qual o FQDN de serviços Web externos irá resolver.</span><span class="sxs-lookup"><span data-stu-id="a704a-121">Must be able to allow binding of a certificate to a listener or interface through which the external web services FQDN will resolve.</span></span> <span data-ttu-id="a704a-122">Configurações de ouvinte são preferíveis para interfaces.</span><span class="sxs-lookup"><span data-stu-id="a704a-122">Listener configurations are preferable to interfaces.</span></span> <span data-ttu-id="a704a-123">Muitos ouvintes podem ser configurados em uma única interface.</span><span class="sxs-lookup"><span data-stu-id="a704a-123">Many listeners can be configured on a single interface.</span></span>

  - <span data-ttu-id="a704a-124">Deve permitir a configuração do controle de cabeçalho de host.</span><span class="sxs-lookup"><span data-stu-id="a704a-124">Must allow for the configuration of host header handling.</span></span> <span data-ttu-id="a704a-125">Geralmente, o cabeçalho original do host enviado pelo cliente solicitante deve ser passado de forma transparente, em vez de ser modificado pelo proxy reverso.</span><span class="sxs-lookup"><span data-stu-id="a704a-125">Often, the original host header sent by the requesting client must be passed transparently, instead of being modified by the reverse proxy.</span></span>

  - <span data-ttu-id="a704a-126">A ponte do tráfego SSL e TLS de uma porta definida externamente (por exemplo, TCP 443) para outra porta definida (por exemplo, TCP 4443).</span><span class="sxs-lookup"><span data-stu-id="a704a-126">Bridging of SSL and TLS traffic from one externally defined port (for example, TCP 443) to another defined port (for example, TCP 4443).</span></span> <span data-ttu-id="a704a-127">O proxy reverso pode descriptografar o pacote no recebimento e, em seguida, criptografar novamente o pacote no envio.</span><span class="sxs-lookup"><span data-stu-id="a704a-127">The reverse proxy may decrypt the packet on receipt and then reencrypt the packet on sending.</span></span>

  - <span data-ttu-id="a704a-128">Conexão de tráfego TCP não criptografado de uma porta (por exemplo, TCP 80) para outro (por exemplo, TCP 8080).</span><span class="sxs-lookup"><span data-stu-id="a704a-128">Bridging of unencrypted TCP traffic from one port (for example, TCP 80) to another (for example, TCP 8080).</span></span>

  - <span data-ttu-id="a704a-129">Permitir a configuração ou aceitar autenticação NTLM, sem autenticação e autenticação de passagem.</span><span class="sxs-lookup"><span data-stu-id="a704a-129">Allow configuration of, or accept, NTLM authentication, No authentication and Pass-through authentication.</span></span>

<span data-ttu-id="a704a-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a704a-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

