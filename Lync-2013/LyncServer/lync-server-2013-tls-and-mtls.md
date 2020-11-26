---
title: 'Lync Server 2013: TLS e MTLS'
description: 'Lync Server 2013: TLS e MTLS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: TLS and MTLS for Lync Server 2013
ms:assetid: b32a5b85-fc82-42dc-a9b2-96400f8cd2b8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481133(v=OCS.15)
ms:contentKeyID: 59893873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a0ccee47e635435dd5f0d5eae03711c0cd5e517b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439693"
---
# <a name="tls-and-mtls-for-lync-server-2013"></a><span data-ttu-id="d4bac-103">TLS e MTLS para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d4bac-103">TLS and MTLS for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d4bac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d4bac-104">

<span> </span></span></span>

<span data-ttu-id="d4bac-105">_**Tópico da última modificação:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="d4bac-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="d4bac-106">Os protocolos Transport Layer Security (TLS) e Mutual Transport Layer Security (MTLS) fornecem comunicações criptografadas e autenticação de ponto de extremidade na Internet.</span><span class="sxs-lookup"><span data-stu-id="d4bac-106">Transport Layer Security (TLS) and Mutual Transport Layer Security (MTLS) protocols provide encrypted communications and endpoint authentication on the Internet.</span></span> <span data-ttu-id="d4bac-107">O Microsoft Lync Server 2013 usa esses dois protocolos para criar a rede de servidores confiáveis e garantir que todas as comunicações na rede sejam criptografadas.</span><span class="sxs-lookup"><span data-stu-id="d4bac-107">Microsoft Lync Server 2013 uses these two protocols to create the network of trusted servers and to ensure that all communications over that network are encrypted.</span></span> <span data-ttu-id="d4bac-108">Todas as comunicações SIP entre servidores ocorrem no MTLS.</span><span class="sxs-lookup"><span data-stu-id="d4bac-108">All SIP communications between servers occur over MTLS.</span></span> <span data-ttu-id="d4bac-109">As comunicações SIP entre o cliente e o servidor ocorrem no TLS.</span><span class="sxs-lookup"><span data-stu-id="d4bac-109">SIP communications from client to server occur over TLS.</span></span>

<span data-ttu-id="d4bac-110">O TLS permite que os usuários, por meio do software cliente, autentiquem os servidores do Lync Server 2013 aos quais se conectam.</span><span class="sxs-lookup"><span data-stu-id="d4bac-110">TLS enables users, through their client software, to authenticate the Lync Server 2013 servers to which they connect.</span></span> <span data-ttu-id="d4bac-111">Em uma conexão TLS, o cliente solicita um certificado válido do servidor.</span><span class="sxs-lookup"><span data-stu-id="d4bac-111">On a TLS connection, the client requests a valid certificate from the server.</span></span> <span data-ttu-id="d4bac-112">Para ser válido, o certificado deve ser emitido por uma AC considerada confiável pelo cliente, e o nome DNS do servidor deve corresponder ao nome DNS no certificado.</span><span class="sxs-lookup"><span data-stu-id="d4bac-112">To be valid, the certificate must have been issued by a CA that is also trusted by the client and the DNS name of the server must match the DNS name on the certificate.</span></span> <span data-ttu-id="d4bac-113">Se o certificado for válido, o cliente usa a chave pública no certificado para criptografar as chaves de criptografia simétricas a serem utilizadas na comunicação, assim, apenas o proprietário original do certificado pode utilizar sua chave privada para descriptografar os conteúdos de comunicação.</span><span class="sxs-lookup"><span data-stu-id="d4bac-113">If the certificate is valid, the client uses the public key in the certificate to encrypt the symmetric encryption keys to be used for the communication, so only the original owner of the certificate can use its private key to decrypt the contents of the communication.</span></span> <span data-ttu-id="d4bac-114">A conexão resultante é confiável e, a partir desse momento, não será desafiada por nenhum outro servidor ou cliente confiável.</span><span class="sxs-lookup"><span data-stu-id="d4bac-114">The resulting connection is trusted and from that point is not challenged by other trusted servers or clients.</span></span> <span data-ttu-id="d4bac-115">Nesse contexto, a Secure Sockets Layer (SSL), conforme utilizada com serviços os Web, pode ser associada ao protocolo baseado em TLS.</span><span class="sxs-lookup"><span data-stu-id="d4bac-115">Within this context, Secure Sockets Layer (SSL) as used with Web services can be associated as TLS-based.</span></span>

<span data-ttu-id="d4bac-116">Conexões de servidor para servidor baseiam-se em MTLS para autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="d4bac-116">Server-to-server connections rely on MTLS for mutual authentication.</span></span> <span data-ttu-id="d4bac-117">Em uma conexão MTLS, o servidor que cria a mensagem e o servidor que a recebe trocam certificados mutuamente a partir de uma AC confiável.</span><span class="sxs-lookup"><span data-stu-id="d4bac-117">On an MTLS connection, the server originating a message and the server receiving it exchange certificates from a mutually trusted CA.</span></span> <span data-ttu-id="d4bac-118">Os certificados comprovam a identidade de cada servidor ao outro.</span><span class="sxs-lookup"><span data-stu-id="d4bac-118">The certificates prove the identity of each server to the other.</span></span> <span data-ttu-id="d4bac-119">Nas implantações do Lync Server 2013, os certificados emitidos pela CA corporativa que estão durante o período de validade e não revogados pela CA de emissão são automaticamente considerados válidos por todos os clientes e servidores internos porque todos os membros de um domínio do Active Directory confiam na CA corporativa nesse domínio.</span><span class="sxs-lookup"><span data-stu-id="d4bac-119">In Lync Server 2013 deployments, certificates issued by the enterprise CA that are during their validity period and not revoked by the issuing CA are automatically considered valid by all internal clients and servers because all members of an Active Directory domain trust the Enterprise CA in that domain.</span></span> <span data-ttu-id="d4bac-120">Em cenários federados, a AC emissora deve ser confiável por ambos os parceiros federados.</span><span class="sxs-lookup"><span data-stu-id="d4bac-120">In federated scenarios, the issuing CA must be trusted by both federated partners.</span></span> <span data-ttu-id="d4bac-121">Cada parceiro pode usar uma AC diferente, se desejado, contanto que a AC também seja considerada confiável pelo outro parceiro.</span><span class="sxs-lookup"><span data-stu-id="d4bac-121">Each partner can use a different CA, if desired, so long as that CA is also trusted by the other partner.</span></span> <span data-ttu-id="d4bac-122">Essa confiabilidade é mais facilmente assegurada pelos Servidores de Borda que possuem o certificado da AC raiz dos parceiros em suas ACs raiz confiáveis ou pelo uso de uma AC de terceiro que seja considerada confiável pelas duas partes.</span><span class="sxs-lookup"><span data-stu-id="d4bac-122">This trust is most easily accomplished by the Edge Servers having the partner’s root CA certificate in their trusted root CAs, or by use of a third-party CA that is trusted by both parties.</span></span>

<span data-ttu-id="d4bac-123">O TLS e MTLS ajudam a evitar a espionagem e ataques a intermediários.</span><span class="sxs-lookup"><span data-stu-id="d4bac-123">TLS and MTLS help prevent both eavesdropping and man-in-the middle attacks.</span></span> <span data-ttu-id="d4bac-124">Em um ataque a intermediários, o invasor redireciona as comunicações entre duas entidades de rede por meio do computador do invasor, sem o conhecimento das partes.</span><span class="sxs-lookup"><span data-stu-id="d4bac-124">In a man-in-the-middle attack, the attacker reroutes communications between two network entities through the attacker’s computer without the knowledge of either party.</span></span> <span data-ttu-id="d4bac-125">A especificação do TLS e do Lync Server 2013 de servidores confiáveis (somente aqueles especificados no construtor de topologia) reduzem o risco de um ataque man-in-the Middle parcialmente na camada do aplicativo usando a criptografia ponto a ponto coordenada usando a criptografia de chave pública entre os dois pontos de extremidade, e um invasor precisa ter um certificado válido e confiável com a chave privada correspondente e emitida para o nome do serviço ao qual o cliente está se comunicando para descriptografar a comunicação.</span><span class="sxs-lookup"><span data-stu-id="d4bac-125">TLS and Lync Server 2013 specification of trusted servers (only those specified in Topology Builder) mitigate the risk of a man-in-the middle attack partially on the application layer by using end-to-end encryption coordinated using the Public Key cryptography between the two endpoints, and an attacker would have to have a valid and trusted certificate with the corresponding private key and issued to the name of the service to which the client is communicating to decrypt the communication.</span></span> <span data-ttu-id="d4bac-126">Em última análise, entretanto, você deve cumprir as práticas recomendadas de segurança em sua infraestrutura de rede (no caso de um DNS corporativo).</span><span class="sxs-lookup"><span data-stu-id="d4bac-126">Ultimately, however, you must follow best security practices with your networking infrastructure (in this case corporate DNS).</span></span> <span data-ttu-id="d4bac-127">O Lync Server 2013 pressupõe que o servidor DNS é confiável da mesma forma que controladores de domínio e catálogos globais são confiáveis, mas o DNS fornece um nível de segurança contra ataques de seqüestro de DNS impedindo que o servidor de um invasor responda com êxito a uma solicitação para o nome falso.</span><span class="sxs-lookup"><span data-stu-id="d4bac-127">Lync Server 2013 assumes that the DNS server is trusted in the same way that domain controllers and global catalogs are trusted, but DNS does provide a level of safeguard against DNS hijack attacks by preventing an attacker’s server from responding successfully to a request to the spoofed name.</span></span>

<span data-ttu-id="d4bac-128">A figura a seguir mostra em alto nível como o Lync Server 2013 usa a MTLS para criar uma rede de servidores confiáveis.</span><span class="sxs-lookup"><span data-stu-id="d4bac-128">The following figure shows at a high level how Lync Server 2013 uses MTLS to create a network of trusted servers.</span></span>

<span data-ttu-id="d4bac-129">**Conexões confiáveis em uma rede do Lync Server**</span><span class="sxs-lookup"><span data-stu-id="d4bac-129">**Trusted connections in a Lync Server network**</span></span>

<span data-ttu-id="d4bac-130">![437749da-c372-4f0d-ac72-ccfd5191696b](images/Dn481133.437749da-c372-4f0d-ac72-ccfd5191696b(OCS.15).jpg "437749da-c372-4f0d-ac72-ccfd5191696b")</span><span class="sxs-lookup"><span data-stu-id="d4bac-130">![437749da-c372-4f0d-ac72-ccfd5191696b](images/Dn481133.437749da-c372-4f0d-ac72-ccfd5191696b(OCS.15).jpg "437749da-c372-4f0d-ac72-ccfd5191696b")</span></span>

<span data-ttu-id="d4bac-131"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d4bac-131"></div>

<span> </span>

</div>

</div>

</span></span></div>

