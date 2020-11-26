---
title: 'Lync Server 2013: autenticação de usuário e cliente'
description: 'Lync Server 2013: autenticação de usuário e de cliente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User and client authentication for Lync Server 2013
ms:assetid: 77f4b62a-f75c-424d-8f02-a6519090015d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481132(v=OCS.15)
ms:contentKeyID: 59893868
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef545dda38e9ab4236e93df769ead393648194cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440784"
---
# <a name="user-and-client-authentication-for-lync-server-2013"></a><span data-ttu-id="32944-103">Autenticação de usuário e cliente para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32944-103">User and client authentication for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32944-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32944-104">

<span> </span></span></span>

<span data-ttu-id="32944-105">_**Tópico da última modificação:** 2013-11-11_</span><span class="sxs-lookup"><span data-stu-id="32944-105">_**Topic Last Modified:** 2013-11-11_</span></span>

<span data-ttu-id="32944-106">Um usuário confiável é aquele cujas credenciais foram autenticadas por um servidor confiável no Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="32944-106">A trusted user is one whose credentials have been authenticated by a trusted server in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="32944-107">Este servidor geralmente é um servidor Standard Edition, um servidor front-end da edição Enterprise ou um diretor.</span><span class="sxs-lookup"><span data-stu-id="32944-107">This server is usually a Standard Edition server, Enterprise Edition Front End Server, or Director.</span></span> <span data-ttu-id="32944-108">O Lync Server 2013 depende dos serviços de domínio Active Directory como o repositório de back-end único confiável de credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="32944-108">Lync Server 2013 relies on Active Directory Domain Services as the single, trusted back-end repository of user credentials.</span></span>

<span data-ttu-id="32944-109">Autenticação é o provisionamento de credenciais de usuário em um servidor confiável.</span><span class="sxs-lookup"><span data-stu-id="32944-109">Authentication is the provision of user credentials to a trusted server.</span></span> <span data-ttu-id="32944-110">O Lync Server 2013 usa os seguintes protocolos de autenticação, dependendo do status e do local do usuário.</span><span class="sxs-lookup"><span data-stu-id="32944-110">Lync Server 2013 uses the following authentication protocols, depending on the status and location of the user.</span></span>

  - <span data-ttu-id="32944-111">**Protocolo de segurança MIT Kerberos versão 5** para usuários internos com credenciais do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32944-111">**MIT Kerberos version 5 security protocol** for internal users with Active Directory credentials.</span></span> <span data-ttu-id="32944-112">O Kerberos exige conectividade do cliente com os serviços de domínio Active Directory, o que é porque ele não pode ser usado para autenticar clientes fora do firewall corporativo.</span><span class="sxs-lookup"><span data-stu-id="32944-112">Kerberos requires client connectivity to Active Directory Domain Services, which is why it cannot be used for authenticating clients outside the corporate firewall.</span></span>

  - <span data-ttu-id="32944-113">**Protocolo NTLM** para usuários com credenciais do Active Directory conectadas de um ponto de extremidade fora do firewall corporativo.</span><span class="sxs-lookup"><span data-stu-id="32944-113">**NTLM protocol** for users with Active Directory credentials who are connecting from an endpoint outside the corporate firewall.</span></span> <span data-ttu-id="32944-114">O serviço de borda do Access passa solicitações de logon para um diretor, se estiver presente ou um servidor front-end para autenticação.</span><span class="sxs-lookup"><span data-stu-id="32944-114">The Access Edge service passes logon requests to a Director, if present, or a Front End Server for authentication.</span></span> <span data-ttu-id="32944-115">O serviço de borda de acesso não realiza nenhuma autenticação.</span><span class="sxs-lookup"><span data-stu-id="32944-115">The Access Edge service itself performs no authentication.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="32944-116">O protocolo NTLM oferece proteção contra ataques mais fraca que o Kerberos; assim, algumas organizações minimizam o uso de NTLM.</span><span class="sxs-lookup"><span data-stu-id="32944-116">NTLM protocol offers weaker attack protection than Kerberos, so some organizations minimize usage of NTLM.</span></span> <span data-ttu-id="32944-117">Como resultado, o acesso ao Lync Server 2013 pode estar restrito a clientes internos ou a clientes conectados por meio de uma conexão VPN ou DirectAccess.</span><span class="sxs-lookup"><span data-stu-id="32944-117">As a result, access to Lync Server 2013 might be restricted to internal or clients connected through a VPN or DirectAccess connection.</span></span>

    
    </div>

  - <span data-ttu-id="32944-p106">**Protocolo Digest** para os chamados usuários anônimos. Usuários anônimos são usuários externos que não possuem credenciais reconhecidas do Active Directory, mas que foram convidados para uma conferência no local e possuem uma chave de conferência válida. A autenticação Digest não é usada para nenhuma outra interação do cliente.</span><span class="sxs-lookup"><span data-stu-id="32944-p106">**Digest protocol** for so-called anonymous users. Anonymous users are outside users who do not have recognized Active Directory credentials but who have been invited to an on-premises conference and possess a valid conference key. Digest authentication is not used for other client interactions.</span></span>

<span data-ttu-id="32944-121">A autenticação do Lync Server 2013 consiste em duas fases:</span><span class="sxs-lookup"><span data-stu-id="32944-121">Lync Server 2013 authentication consists of two phases:</span></span>

1.  <span data-ttu-id="32944-122">Uma associação de segurança é estabelecida entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="32944-122">A security association is established between the client and the server.</span></span>

2.  <span data-ttu-id="32944-p107">O cliente e o servidor usam a associação de segurança existente para assinar mensagens enviadas e para verificar as mensagens recebidas. Mensagens não autenticadas de um cliente não são aceitas quando uma autenticação está habilitada no servidor.</span><span class="sxs-lookup"><span data-stu-id="32944-p107">The client and server use the existing security association to sign messages that they send and to verify the messages they receive. Unauthenticated messages from a client are not accepted when authentication is enabled on the server.</span></span>

<span data-ttu-id="32944-p108">Uma marca da confiança do usuário é anexada a cada mensagem originária de um usuário, não à identidade do usuário em si. O servidor verifica se há credenciais de usuário válidas em cada mensagem. Se as credenciais de usuário forem válidas, a mensagem não será contestada nem pelo primeiro servidor, nem pelos outros servidores da nuvem de servidores confiáveis.</span><span class="sxs-lookup"><span data-stu-id="32944-p108">User trust is attached to each message that originates from a user, not to the user identity itself. The server checks each message for valid user credentials. If the user credentials are valid, the message is unchallenged not only by the first server to receive it but by all other servers in the trusted server cloud.</span></span>

<span data-ttu-id="32944-128">Usuários com credenciais válidas emitidas por um parceiro federado são confiáveis, porém são opcionalmente impedidos por restrições adicionais de aproveitar toda a gama de privilégios concedidos aos usuários internos.</span><span class="sxs-lookup"><span data-stu-id="32944-128">Users with valid credentials issued by a federated partner are trusted but optionally prevented by additional constraints from enjoying the full range of privileges accorded to internal users.</span></span>

<span data-ttu-id="32944-129">Os protocolos ICE e TURN também utilizam o mecanismo de desafio Digest, conforme descrito no IETF TURN RFC.</span><span class="sxs-lookup"><span data-stu-id="32944-129">The ICE and TURN protocols also use the Digest challenge as described in the IETF TURN RFC.</span></span>

<span data-ttu-id="32944-130">Os certificados de cliente fornecem uma maneira alternativa para os usuários serem autenticados pelo Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="32944-130">Client certificates provide an alternate way for users to be authenticated by Lync Server 2013.</span></span> <span data-ttu-id="32944-131">Em vez de fornecer um nome de usuário e senha, os usuários possuem um certificado e a chave privada correspondente ao certificado exigida para resolver um desafio criptográfico.</span><span class="sxs-lookup"><span data-stu-id="32944-131">Instead of providing a user name and password, users have a certificate and the private key corresponding to the certificate that is required to resolve a cryptographic challenge.</span></span> <span data-ttu-id="32944-132">(Esse certificado deve ter um nome de assunto ou um nome alternativo de assunto que identifique o usuário e deve ser emitido por uma autoridade de certificação raiz que seja confiável para os servidores que executam o Lync Server 2013, estando dentro do período de validade do certificado e não foram revogados.) Para ser autenticado, os usuários só precisam digitar um PIN (número de identificação pessoal).</span><span class="sxs-lookup"><span data-stu-id="32944-132">(This certificate must have a subject name or subject alternative name that identifies the user and must be issued by a Root CA that is trusted by servers running Lync Server 2013, be within the certificate’s validity period, and not have been revoked.) To be authenticated, users only need to type in a personal identification number (PIN).</span></span> <span data-ttu-id="32944-133">Os certificados são especialmente úteis para telefones e outros dispositivos que executam o Microsoft Lync 2013 Phone Edition, no qual é difícil digitar um nome de usuário e/ou senha.</span><span class="sxs-lookup"><span data-stu-id="32944-133">Certificates are particularly useful for telephones and other devices running Microsoft Lync 2013 Phone Edition where it is difficult to enter a user name and/or password.</span></span>

<span data-ttu-id="32944-134"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32944-134"></div>

<span> </span>

</div>

</div>

</span></span></div>

