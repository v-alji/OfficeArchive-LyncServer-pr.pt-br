---
title: 'Lync Server 2013: Extensões, classes e atributos do esquema do Active Directory usado pelo Lync Server'
description: 'Lync Server 2013: extensões de esquema do Active Directory, classes e atributos usados pelo Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory schema extensions, classes, and attributes used by Lync Server 2013
ms:assetid: 579bfa5a-9443-46dd-9a8e-07d00ba2824d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398379(v=OCS.15)
ms:contentKeyID: 48184188
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: beac778d3315573f4d5cc6cb9c827a3a2fce9d0e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389727"
---
# <a name="active-directory-schema-extensions-classes-and-attributes-used-by-lync-server-2013"></a><span data-ttu-id="9a62f-103">Extensões, classes e atributos do esquema do Active Directory usado pelo Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a62f-103">Active Directory schema extensions, classes, and attributes used by Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a62f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a62f-104">

<span> </span></span></span>

<span data-ttu-id="9a62f-105">_**Tópico da última modificação:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="9a62f-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="9a62f-106">Esta seção de referência inclui as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="9a62f-106">This reference section includes the following information:</span></span>

  - <span data-ttu-id="9a62f-107">Extensões de esquema do Active Directory novas ou alteradas para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a62f-107">Active Directory schema extensions that are new or changed for Lync Server 2013</span></span>
    
    <span data-ttu-id="9a62f-108">O esquema do Active Directory contém definições formais de cada classe de objeto que podem ser criadas em uma floresta do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9a62f-108">The Active Directory schema contains formal definitions of every object class that can be created in an Active Directory forest.</span></span> <span data-ttu-id="9a62f-109">O esquema também contém definições formais de cada atributo que podem existir em um objeto do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9a62f-109">The schema also contains formal definitions of every attribute that can exist on an Active Directory object.</span></span> <span data-ttu-id="9a62f-110">O catálogo global do Active Directory contém réplicas de todos os objetos da floresta, juntamente com um subconjunto de atributos para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="9a62f-110">The Active Directory global catalog contains replicas of all the objects for the forest, along with a subset of the attributes for each object.</span></span> <span data-ttu-id="9a62f-111">Esta seção descreve as classes e os atributos que são novos ou alterados no Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9a62f-111">This section describes the classes and attributes that are new or changed in Lync Server 2013.</span></span>

  - <span data-ttu-id="9a62f-112">Todas as classes usadas pelo Lync Server, com uma descrição de cada</span><span class="sxs-lookup"><span data-stu-id="9a62f-112">All the classes used by Lync Server, with a description of each</span></span>

  - <span data-ttu-id="9a62f-113">Todos os atributos usados pelo Lync Server, com uma descrição de cada um</span><span class="sxs-lookup"><span data-stu-id="9a62f-113">All the attributes used by Lync Server, with a description of each</span></span>

  - <span data-ttu-id="9a62f-114">Uma lista das classes usadas pelo Lync Server, com os atributos que cada uma pode conter</span><span class="sxs-lookup"><span data-stu-id="9a62f-114">A list of the classes used by Lync Server, with the attributes each may contain</span></span>

  - <span data-ttu-id="9a62f-115">Configurações e objetos globais, além dos grupos de administração e serviço universal criados durante a preparação da floresta</span><span class="sxs-lookup"><span data-stu-id="9a62f-115">Global settings and objects, in addition to the universal service and administration groups that are created during forest preparation</span></span>

  - <span data-ttu-id="9a62f-116">ACEs (entradas de controle de acesso) criadas na raiz do domínio e nos contêineres internos durante a preparação do domínio</span><span class="sxs-lookup"><span data-stu-id="9a62f-116">Access control entries (ACEs) that are created on the domain root and built-in containers during domain preparation</span></span>

  - <span data-ttu-id="9a62f-117">Alterações feitas em uma UO (unidade organizacional) do Active Directory pelo \_ cmdlet Grant CsSetupPermission.</span><span class="sxs-lookup"><span data-stu-id="9a62f-117">Changes that are made on an Active Directory organizational unit (OU) by the Grant\_CsSetupPermission cmdlet.</span></span>

  - <span data-ttu-id="9a62f-118">Alterações feitas em uma UO do Active Directory pelo \_ cmdlet Grant CsOUPermission.</span><span class="sxs-lookup"><span data-stu-id="9a62f-118">Changes that are made on an Active Directory OU by the Grant\_CsOUPermission cmdlet.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9a62f-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9a62f-119">In This Section</span></span>

  - [<span data-ttu-id="9a62f-120">Alterações de esquema no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a62f-120">Schema changes in Lync Server 2013</span></span>](lync-server-2013-schema-changes-in-lync-server-2013.md)

  - [<span data-ttu-id="9a62f-121">Classes e descrições de esquema no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a62f-121">Schema classes and descriptions in Lync Server 2013</span></span>](lync-server-2013-schema-classes-and-descriptions.md)

  - [<span data-ttu-id="9a62f-122">Atributos e descrições de esquema no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a62f-122">Schema attributes and descriptions in Lync Server 2013</span></span>](lync-server-2013-schema-attributes-and-descriptions.md)

  - [<span data-ttu-id="9a62f-123">Atributos de esquema por classe no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a62f-123">Schema attributes by class in Lync Server 2013</span></span>](lync-server-2013-schema-attributes-by-class.md)

  - [<span data-ttu-id="9a62f-124">Alterações feitas pela preparação da floresta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a62f-124">Changes made by forest preparation in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-forest-preparation.md)

  - [<span data-ttu-id="9a62f-125">Alterações feitas por preparação do domínio no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a62f-125">Changes made by domain preparation in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-domain-preparation.md)

  - [<span data-ttu-id="9a62f-126">Alterações feitas por Grant-CsSetupPermission no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a62f-126">Changes made by Grant-CsSetupPermission in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission)

  - [<span data-ttu-id="9a62f-127">Alterações feitas por Grant-CsOUPermission no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a62f-127">Changes made by Grant-CsOUPermission in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-https://docs.microsoft.com/powershell/module/skype/Grant-CsOUPermission)

<span data-ttu-id="9a62f-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a62f-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

