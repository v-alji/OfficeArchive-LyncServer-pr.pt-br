---
title: 'Lync Server 2013: Pré-requisitos para habilitar autenticação Kerberos'
description: 'Lync Server 2013: pré-requisitos para habilitar a autenticação Kerberos.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prerequisites for enabling Kerberos authentication
ms:assetid: 3f276a21-7476-4bc0-9fd1-59e844d2e9c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425909(v=OCS.15)
ms:contentKeyID: 48183945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 65a45bad0eb249fdbc717fe05f080ce737c87c6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436969"
---
# <a name="prerequisites-for-enabling-kerberos-authentication-in-lync-server-2013"></a><span data-ttu-id="861a5-103">Pré-requisitos para habilitar autenticação Kerberos no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="861a5-103">Prerequisites for enabling Kerberos authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="861a5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="861a5-104">

<span> </span></span></span>

<span data-ttu-id="861a5-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="861a5-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="861a5-106">Antes de habilitar a autenticação Kerberos, certifique-se de concluir todas as preparações de configuração e infraestrutura:</span><span class="sxs-lookup"><span data-stu-id="861a5-106">Before enabling Kerberos authentication, make sure that you complete all prerequisite configuration and infrastructure preparations:</span></span>

  - <span data-ttu-id="861a5-107">O esquema do Active Directory é estendido para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="861a5-107">Active Directory schema is extended for Lync Server 2013.</span></span>

  - <span data-ttu-id="861a5-108">A preparação da floresta do Active Directory é concluída para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="861a5-108">Active Directory forest preparation is completed for Lync Server 2013.</span></span>

  - <span data-ttu-id="861a5-109">A preparação do domínio do Active Directory foi concluída para o Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="861a5-109">Active Directory domain preparation is completed for Lync Server 2013.</span></span>

  - <span data-ttu-id="861a5-110">O repositório de gerenciamento central foi instalado e está disponível com êxito.</span><span class="sxs-lookup"><span data-stu-id="861a5-110">Central Management store is successfully installed and available.</span></span>

  - <span data-ttu-id="861a5-111">A topologia foi criada e publicada usando o construtor de topologias.</span><span class="sxs-lookup"><span data-stu-id="861a5-111">The topology has been created and published by using Topology Builder.</span></span>

  - <span data-ttu-id="861a5-112">Os servidores e funções que exigem serviços Web foram definidos e implantados, incluindo servidores front-end, servidores de edição padrão e directors.</span><span class="sxs-lookup"><span data-stu-id="861a5-112">Servers and roles that require Web Services have been defined and deployed, including Front End Servers, Standard Edition servers, and Directors.</span></span>

  - <span data-ttu-id="861a5-113">Os serviços de informações da Internet (IIS) são configurados e implantados com os serviços de função recomendados para dar suporte a serviços Web no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="861a5-113">Internet Information Services (IIS) is configured and deployed with the recommended role services to support Web Services in Lync Server 2013.</span></span>

<span data-ttu-id="861a5-114">Depois que os pré-requisitos forem atendidos, você deve estar pronto para criar uma ou mais contas para serviços Web a serem usados para a autenticação Kerberos para a implantação.</span><span class="sxs-lookup"><span data-stu-id="861a5-114">After the prerequisites have been met, you should be ready to create one or more accounts for Web Services to use for Kerberos authentication for your deployment.</span></span> <span data-ttu-id="861a5-115">No mínimo, você precisa criar uma conta de autenticação Kerberos para cada implantação.</span><span class="sxs-lookup"><span data-stu-id="861a5-115">At a minimum, you need to create one Kerberos authentication account for each deployment.</span></span> <span data-ttu-id="861a5-116">No entanto, você pode criar uma conta para cada site para fornecer autenticação Kerberos local no site.</span><span class="sxs-lookup"><span data-stu-id="861a5-116">However, you can create an account for each site to provide local Kerberos authentication at the site.</span></span> <span data-ttu-id="861a5-117">Você só pode especificar uma conta de autenticação Kerberos por site.</span><span class="sxs-lookup"><span data-stu-id="861a5-117">You can only specify one Kerberos authentication account per site.</span></span>

<span data-ttu-id="861a5-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="861a5-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

