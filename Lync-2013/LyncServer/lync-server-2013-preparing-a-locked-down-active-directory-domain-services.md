---
title: 'Lync Server 2013: Preparando Serviços de Domínio Active Directory bloqueado'
description: 'Lync Server 2013: preparando os serviços de domínio do Active Directory bloqueados.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing a locked-down Active Directory Domain Services
ms:assetid: 68bde963-3fa3-4102-88d6-ac931c1dd2d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398492(v=OCS.15)
ms:contentKeyID: 48184377
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4aea04b138de2630935713eda7cbef9e4d21572a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424223"
---
# <a name="preparing-a-locked-down-active-directory-domain-services-in-lync-server-2013"></a><span data-ttu-id="15309-103">Preparando Serviços de Domínio Active Directory bloqueado no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15309-103">Preparing a locked-down Active Directory Domain Services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15309-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15309-104">

<span> </span></span></span>

<span data-ttu-id="15309-105">_**Tópico da última modificação:** 2012-05-14_</span><span class="sxs-lookup"><span data-stu-id="15309-105">_**Topic Last Modified:** 2012-05-14_</span></span>

<span data-ttu-id="15309-106">Geralmente, as organizações bloqueiam os serviços de domínio do Active Directory para ajudar a reduzir os riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="15309-106">Organizations often lock down Active Directory Domain Services to help mitigate security risks.</span></span> <span data-ttu-id="15309-107">No entanto, um ambiente do Active Directory bloqueado pode limitar as permissões exigidas pelo Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="15309-107">However, a locked-down Active Directory environment can limit the permissions that Lync Server 2013 requires.</span></span> <span data-ttu-id="15309-108">A preparação adequada de um ambiente do Active Directory bloqueado para o Lync Server 2013 envolve algumas considerações e etapas adicionais.</span><span class="sxs-lookup"><span data-stu-id="15309-108">Properly preparing a locked-down Active Directory environment for Lync Server 2013 involves some additional considerations and steps.</span></span>

<span data-ttu-id="15309-109">Duas maneiras comuns nas quais as permissões são limitadas em um ambiente bloqueado do Active Directory são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="15309-109">Two common ways in which permissions are limited in a locked-down Active Directory environment are as follows:</span></span>

  - <span data-ttu-id="15309-110">As entradas de controle de acesso do usuário autenticado (ACEs) são removidas dos contêineres.</span><span class="sxs-lookup"><span data-stu-id="15309-110">Authenticated user access control entries (ACEs) are removed from containers.</span></span>

  - <span data-ttu-id="15309-111">A herança de permissões está desabilitada em contêineres de objetos de usuário, contato, InetOrgPerson ou computador.</span><span class="sxs-lookup"><span data-stu-id="15309-111">Permissions inheritance is disabled on containers of User, Contact, InetOrgPerson, or Computer objects.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="15309-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="15309-112">In This Section</span></span>

  - [<span data-ttu-id="15309-113">Permissões de usuário autenticado são removidas no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15309-113">Authenticated user permissions are removed in Lync Server 2013</span></span>](lync-server-2013-authenticated-user-permissions-are-removed.md)

  - [<span data-ttu-id="15309-114">Herança de permissões está desabilitado em computadores, usuários ou contêiners InetOrgPerson no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15309-114">Permissions inheritance Is disabled on computers, users, or InetOrgPerson containers in Lync Server 2013</span></span>](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md)

<span data-ttu-id="15309-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15309-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

