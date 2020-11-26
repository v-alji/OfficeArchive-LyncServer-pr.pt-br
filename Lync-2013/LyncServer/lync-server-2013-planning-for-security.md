---
title: 'Lync Server 2013: Planejando a segurança'
description: 'Lync Server 2013: planejando a segurança.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for security
ms:assetid: 17eeba87-cafa-4e9b-852d-c017a7d10d59
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn342827(v=OCS.15)
ms:contentKeyID: 56107267
ms.date: 06/22/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1abc02aa3f42a6b12c66c621b071e0b3ddb545c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424440"
---
# <a name="planning-for-security-in-lync-server-2013"></a><span data-ttu-id="3e71f-103">Planejando a segurança no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e71f-103">Planning for security in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e71f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e71f-104">

<span> </span></span></span>

<span data-ttu-id="3e71f-105">_**Tópico da última modificação:** 2016-06-22_</span><span class="sxs-lookup"><span data-stu-id="3e71f-105">_**Topic Last Modified:** 2016-06-22_</span></span>

<span data-ttu-id="3e71f-106">Use esta seção de segurança para avaliar e gerenciar riscos de segurança na sua implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3e71f-106">Use this security section to assess and manage security risks to your deployment of Lync Server 2013.</span></span>

<span data-ttu-id="3e71f-107">Mesmo que a implantação do Lync Server 2013 seja modesto, é provável que você tenha componentes da sua rede com sua própria documentação de segurança.</span><span class="sxs-lookup"><span data-stu-id="3e71f-107">Even if your Lync Server 2013 deployment is modest, you probably have components in your network that have their own security documentation.</span></span> <span data-ttu-id="3e71f-108">Portanto, é improvável que esta seção cubra todos os aspectos de segurança para todos os componentes e áreas pertinentes à sua implantação.</span><span class="sxs-lookup"><span data-stu-id="3e71f-108">Therefore, it is unlikely that this section covers all aspects of security for all components and areas that are pertinent to your deployment.</span></span>

<span data-ttu-id="3e71f-109">Use esta seção como ponto de partida para solucionar a segurança da sua implantação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3e71f-109">Use this section as a starting point to address the security of your Lync Server 2013 deployment.</span></span> <span data-ttu-id="3e71f-110">Ele fornece diretrizes gerais e práticas recomendadas para avaliar e gerenciar os riscos de segurança mais comuns.</span><span class="sxs-lookup"><span data-stu-id="3e71f-110">It provides general guidelines and best practices for assessing and managing the most common security risks.</span></span> <span data-ttu-id="3e71f-111">Recursos de segurança e produtos adicionais estão listados no final de cada tópico.</span><span class="sxs-lookup"><span data-stu-id="3e71f-111">Additional product and security resources are listed at the end of each topic.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3e71f-112">A segurança é um tópico em constante evolução.</span><span class="sxs-lookup"><span data-stu-id="3e71f-112">Security is a constantly evolving topic.</span></span> <span data-ttu-id="3e71f-113">Como surgem novas ameaças e soluções, documentos, soluções, métodos e procedimentos desatualizados devem ser substituídos por um material atualizado.</span><span class="sxs-lookup"><span data-stu-id="3e71f-113">As new threats and solutions arise, outdated documents, solutions, methods, and procedures should be replaced with up-to-date material.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3e71f-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3e71f-114">In This Section</span></span>

  - [<span data-ttu-id="3e71f-115">Recursos de segurança-chave no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e71f-115">Key security features in Lync Server 2013</span></span>](lync-server-2013-key-security-features.md)

  - [<span data-ttu-id="3e71f-116">Ameaças de segurança comuns no Modern Day Computing</span><span class="sxs-lookup"><span data-stu-id="3e71f-116">Common security threats in modern day computing</span></span>](lync-server-2013-common-security-threats-in-modern-day-computing.md)

  - [<span data-ttu-id="3e71f-117">Exclusões de verificação de antivírus para Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e71f-117">Antivirus scanning exclusions for Lync Server 2013</span></span>](lync-server-2013-antivirus-scanning-exclusions.md)

  - [<span data-ttu-id="3e71f-118">Estrutura de segurança do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e71f-118">Security framework for Lync Server 2013</span></span>](lync-server-2013-security-framework-for-lync-server.md)

  - [<span data-ttu-id="3e71f-119">Lidando com ameaças à sua infraestrutura principal do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e71f-119">Addressing threats to your core infrastructure for Lync Server 2013</span></span>](lync-server-2013-addressing-threats-to-your-core-infrastructure.md)

  - [<span data-ttu-id="3e71f-120">Implantando porta não padrão e alias do SQL Server no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e71f-120">Deploying a SQL Server nonstandard port and alias in Lync Server 2013</span></span>](deploying-a-sql-server-nonstandard-port-and-alias-in-lync-server-2013.md)

<span data-ttu-id="3e71f-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e71f-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

