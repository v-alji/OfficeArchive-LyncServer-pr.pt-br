---
title: 'Lync Server 2013: Configurando o suporte de Federação para um cliente do Lync Online'
description: 'Lync Server 2013: Configurando o suporte de Federação para um cliente do Lync Online.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring federation support for a Lync Online customer
ms:assetid: e5f7f38d-ede5-4af3-88c2-026e8a78df12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202193(v=OCS.15)
ms:contentKeyID: 48185669
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b5e7995e686a9492b3a4be98a92b848716cacf9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433112"
---
# <a name="configuring-federation-support-for-a-lync-online-customer-in-lync-server-2013"></a><span data-ttu-id="a300c-103">Configurando o suporte de Federação para um cliente do Lync Online no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a300c-103">Configuring federation support for a Lync Online customer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a300c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a300c-104">

<span> </span></span></span>

<span data-ttu-id="a300c-105">_**Tópico da última modificação:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a300c-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a300c-106">Você pode fornecer serviços de comunicação para os usuários de sua organização de qualquer uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="a300c-106">You can provide communications services to users in your organization in any of the following ways:</span></span>

  - <span data-ttu-id="a300c-107">Implantar o Lync Server 2013 em sua organização (conhecido como *serviços locais*) e configurar as contas de usuário do Lync 2013 em sua organização.</span><span class="sxs-lookup"><span data-stu-id="a300c-107">Deploying Lync Server 2013 in your organization (known as *on-premises services*) and setting up Lync 2013 user accounts in your organization.</span></span>

  - <span data-ttu-id="a300c-108">Configurar uma conta de cliente do Microsoft Lync Online 2010 com um provedor de hospedagem e configurar contas de usuário com o provedor de hospedagem (conhecido como *serviços online*).</span><span class="sxs-lookup"><span data-stu-id="a300c-108">Setting up a Microsoft Lync Online 2010 customer account with a Hosting Provider and setting up user accounts with the Hosting Provider (known as *online services*).</span></span>

<span data-ttu-id="a300c-109">Se você implantar o Lync 2013 em sua organização, poderá federar-se com os domínios de um ou mais clientes do Microsoft Lync Online 2010.</span><span class="sxs-lookup"><span data-stu-id="a300c-109">If you deploy Lync 2013 in your organization, you can federate with the domains of one or more Microsoft Lync Online 2010 customers.</span></span> <span data-ttu-id="a300c-110">Para habilitar a Federação entre os usuários da implantação do Lync 2013 local e dos usuários de um cliente do Lync Online 2010, você deve configurar o suporte para o domínio e usuários do cliente do Lync Online.</span><span class="sxs-lookup"><span data-stu-id="a300c-110">To enable federation between users of your on-premises Lync 2013 deployment and users of a Lync Online 2010 customer, you must configure support for the domain and users of the Lync Online customer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a300c-111">Esta documentação descreve apenas os procedimentos para configurar sua organização para dar suporte à Federação com um cliente do Lync Online 2010.</span><span class="sxs-lookup"><span data-stu-id="a300c-111">This documentation describes only the procedures for configuring your organization to support federation with an Lync Online 2010 customer.</span></span> <span data-ttu-id="a300c-112">Esta documentação não descreve os procedimentos para configurar o cliente do Lync Online 2010 para dar suporte à Federação.</span><span class="sxs-lookup"><span data-stu-id="a300c-112">This documentation does not describe the procedures for configuring the Lync Online 2010 customer to support federation.</span></span> <span data-ttu-id="a300c-113">Para obter detalhes sobre os serviços do Lync Online, consulte Lync Online em <A href="https://go.microsoft.com/fwlink/p/?linkid=218941">https://go.microsoft.com/fwlink/p/?linkId=218941</A> .</span><span class="sxs-lookup"><span data-stu-id="a300c-113">For details about Lync Online services, see Lync Online at <A href="https://go.microsoft.com/fwlink/p/?linkid=218941">https://go.microsoft.com/fwlink/p/?linkId=218941</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a300c-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a300c-114">In This Section</span></span>

  - [<span data-ttu-id="a300c-115">Pré-requisitos para federação com um cliente do Lync Online no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a300c-115">Prerequisites for federating with a Lync Online customer in Lync Server 2013</span></span>](lync-server-2013-prerequisites-for-federating-with-a-lync-online-customer.md)

  - [<span data-ttu-id="a300c-116">Configurar o suporte de Federação para um domínio do Lync Online no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a300c-116">Configure federation support for a Lync Online domain in Lync Server 2013</span></span>](lync-server-2013-configure-federation-support-for-a-lync-online-domain.md)

  - [<span data-ttu-id="a300c-117">Configurar o acesso do usuário para federação com um cliente do Lync Online no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a300c-117">Configure user access for federation with a Lync Online customer in Lync Server 2013</span></span>](lync-server-2013-configure-user-access-for-federation-with-a-lync-online-customer.md)

  - [<span data-ttu-id="a300c-118">Verificar comunicações com um cliente do Lync Online no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a300c-118">Verify communications with a Lync Online customer in Lync Server 2013</span></span>](lync-server-2013-verify-communications-with-a-lync-online-customer.md)

<span data-ttu-id="a300c-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a300c-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

