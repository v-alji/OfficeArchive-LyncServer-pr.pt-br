---
title: 'Lync Server 2013: Implantação de acesso do usuário externo'
description: 'Lync Server 2013: Implantando o acesso de usuários externos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying external user access
ms:assetid: d40c9574-c16b-4fe6-b848-21ae0b7e4f0e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398918(v=OCS.15)
ms:contentKeyID: 48185495
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af41a169fe3a72e440e95cfa370a16117fb828a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430004"
---
# <a name="deploying-external-user-access-in-lync-server-2013"></a><span data-ttu-id="3bd75-103">Implantação de acesso do usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bd75-103">Deploying external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3bd75-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3bd75-104">

<span> </span></span></span>

<span data-ttu-id="3bd75-105">_**Tópico da última modificação:** 2013-09-23_</span><span class="sxs-lookup"><span data-stu-id="3bd75-105">_**Topic Last Modified:** 2013-09-23_</span></span>

<span data-ttu-id="3bd75-106">A implantação de componentes de borda do Microsoft Lync Server 2013 possibilita a usuários externos que não estão conectados à rede interna da sua organização, incluindo usuários remotos autenticados e anônimos, parceiros federados (incluindo parceiros do XMPP), clientes móveis e usuários de serviços de mensagens instantâneas (IM), para se comunicar com outros usuários em sua organização usando o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="3bd75-106">Deploying edge components for Microsoft Lync Server 2013 makes it possible for external users who are not logged into your organization’s internal network, including authenticated and anonymous remote users, federated partners (including XMPP partners), mobile clients and users of public instant messaging (IM) services, to communicate with other users in your organization using Lync Server.</span></span> <span data-ttu-id="3bd75-107">Os processos de implantação e configuração do Lync Server 2013 não são significativamente diferentes do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3bd75-107">The deployment and configuration processes for Lync Server 2013 are not significantly different from Lync Server 2010.</span></span> <span data-ttu-id="3bd75-108">As ferramentas de instalação e administração são muito parecidas com as do Lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3bd75-108">The tools for installation and administration are much the same as in Lync Server 2010.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3bd75-109">A instalação e a configuração do servidor de borda do Microsoft Lync Server 2013 &nbsp; podem ser um processo complexo que exija uma quantia potencialmente significativa de planejamento e coordenação com suas equipes internas, incluindo, entre outros, segurança, rede, firewall, sistema de nome de domínio (DNS), balanceamento de carga e considerações sobre a PKI (infraestrutura de chave pública).</span><span class="sxs-lookup"><span data-stu-id="3bd75-109">Microsoft Lync Server 2013&nbsp;Edge Server installation and configuration can be a complex process requiring a potentially significant amount of planning and coordination with your internal teams, including – but not limited to – security, networking, firewall, domain name system (DNS), load balancer, and public key infrastructure (PKI) considerations.</span></span> <span data-ttu-id="3bd75-110">É altamente recomendável que você examine e use o processo de planejamento e a documentação fornecida antes de implantar seus componentes de acesso externo.</span><span class="sxs-lookup"><span data-stu-id="3bd75-110">It is strongly recommended that you review and use the planning process and documentation provided before deploying your external access components.</span></span> <span data-ttu-id="3bd75-111">Isso ajudará a limitar o número e a frequência de alterações não desejadas e problemas à medida que você passar pelo processo de implantação.</span><span class="sxs-lookup"><span data-stu-id="3bd75-111">This will assist in limiting the number and frequency of undesired changes and problems as you proceed through the deployment process.</span></span> <span data-ttu-id="3bd75-112">Para obter informações sobre como planejar o acesso de usuários externos, consulte <A href="lync-server-2013-planning-for-external-user-access.md">planejar o acesso de usuários externos no Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="3bd75-112">For information on planning you external user access, see <A href="lync-server-2013-planning-for-external-user-access.md">Planning for external user access in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3bd75-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3bd75-113">In This Section</span></span>

  - [<span data-ttu-id="3bd75-114">Llista de verificação de implantação para acesso de usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bd75-114">Deployment checklist for external user access in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-external-user-access.md)

  - [<span data-ttu-id="3bd75-115">Requisitos do sistema para componentes de acesso de usuário externo para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bd75-115">System requirements for external user access components for Lync Server 2013</span></span>](lync-server-2013-system-requirements-for-external-user-access-components.md)

  - [<span data-ttu-id="3bd75-116">Preparando para instalação de servidores na rede de perímetro para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bd75-116">Preparing for installation of servers in the perimeter network for Lync Server 2013</span></span>](lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md)

  - [<span data-ttu-id="3bd75-117">Criando uma topologia de borda e de diretor no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bd75-117">Building an edge and Director topology in Lync Server 2013</span></span>](lync-server-2013-building-an-edge-and-director-topology.md)

  - <span data-ttu-id="3bd75-118">[Configurando o diretor no Lync Server 2013](lync-server-2013-setting-up-the-director.md) (opcional)</span><span class="sxs-lookup"><span data-stu-id="3bd75-118">[Setting up the Director in Lync Server 2013](lync-server-2013-setting-up-the-director.md) (optional)</span></span>

  - [<span data-ttu-id="3bd75-119">Configurando os servidores de borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bd75-119">Setting up Edge Servers in Lync Server 2013</span></span>](lync-server-2013-setting-up-edge-servers.md)

  - [<span data-ttu-id="3bd75-120">Configurando servidores de proxy reverso para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bd75-120">Setting up reverse proxy servers for Lync Server 2013</span></span>](lync-server-2013-setting-up-reverse-proxy-servers.md)

  - [<span data-ttu-id="3bd75-121">Configurando suporte para acesso de usuário externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bd75-121">Configuring support for external user access in Lync Server 2013</span></span>](lync-server-2013-configuring-support-for-external-user-access.md)

  - [<span data-ttu-id="3bd75-122">Guia de configuração para conectividade Lync-Skype no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bd75-122">Provisioning guide for Lync-Skype connectivity in Lync Server 2013</span></span>](lync-server-2013-provisioning-guide-for-lync-skype-connectivity.md)

  - [<span data-ttu-id="3bd75-123">Configurando federação SIP, federação XMPP e sistema de mensagens instântaneas público no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bd75-123">Configuring SIP federation, XMPP federation and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md)

  - [<span data-ttu-id="3bd75-124">Implantando mobilidade no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bd75-124">Deploying mobility in Lync Server 2013</span></span>](lync-server-2013-deploying-mobility.md)

  - [<span data-ttu-id="3bd75-125">Verificando a implantação de borda no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bd75-125">Verifying your edge deployment in Lync Server 2013</span></span>](lync-server-2013-verifying-your-edge-deployment.md)

<span data-ttu-id="3bd75-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3bd75-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

