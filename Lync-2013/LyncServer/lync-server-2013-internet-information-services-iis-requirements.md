---
title: 'Lync Server 2013: Requisitos de Serviços de Informações da Internet (IIS)'
description: 'Lync Server 2013: requisitos dos serviços de informações da Internet (IIS).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Internet Information Services (IIS) requirements
ms:assetid: 4f57a605-a8a9-4c5a-9a18-05ecb3d9ab6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398321(v=OCS.15)
ms:contentKeyID: 48184128
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd8de55fa4611c3ab29eac7d7c28c522b418e77d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426849"
---
# <a name="internet-information-services-iis-requirements-in-lync-server-2013"></a><span data-ttu-id="c0385-103">Requisitos de Serviços de Informações da Internet (IIS) no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0385-103">Internet Information Services (IIS) requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0385-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0385-104">

<span> </span></span></span>

<span data-ttu-id="c0385-105">_**Tópico da última modificação:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="c0385-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="c0385-106">Vários componentes do Lync Server 2013 exigem serviços de informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="c0385-106">Several Lync Server 2013 components require Internet Information Services (IIS).</span></span> <span data-ttu-id="c0385-107">Este tópico descreve os recursos específicos do IIS necessários para dar suporte ao Lync Server.</span><span class="sxs-lookup"><span data-stu-id="c0385-107">This topic describes the specific IIS features required to support Lync Server.</span></span> <span data-ttu-id="c0385-108">Os tópicos desta seção descrevem os requisitos de componentes específicos para o IIS.</span><span class="sxs-lookup"><span data-stu-id="c0385-108">The topics in this section describe the requirements of specific components for IIS.</span></span>

<span data-ttu-id="c0385-109">Quando a função servidor Web (IIS) estiver habilitada no Windows Server 2008, vários serviços de função serão instalados por padrão.</span><span class="sxs-lookup"><span data-stu-id="c0385-109">When the Web Server (IIS) role is enabled on Windows Server 2008, various role services are installed by default.</span></span> <span data-ttu-id="c0385-110">A tabela a seguir descreve os serviços de função adicionais que devem ser instalados quando a função do servidor Web (IIS) estiver habilitada no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c0385-110">The following table describes the additional role services that must be installed when the Web Server (IIS) role is enabled on Windows Server 2008.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0385-111">Serviço de função</span><span class="sxs-lookup"><span data-stu-id="c0385-111">Role service</span></span></th>
<th><span data-ttu-id="c0385-112">Recurso</span><span class="sxs-lookup"><span data-stu-id="c0385-112">Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0385-113">Recursos HTTP Comuns</span><span class="sxs-lookup"><span data-stu-id="c0385-113">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="c0385-114">Redirecionamento de HTTP</span><span class="sxs-lookup"><span data-stu-id="c0385-114">HTTP Redirection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0385-115">Desenvolvimento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="c0385-115">Application Development</span></span></p></td>
<td><p><span data-ttu-id="c0385-116">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="c0385-116">ASP.NET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0385-117">Desenvolvimento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="c0385-117">Application Development</span></span></p></td>
<td><p><span data-ttu-id="c0385-118">Extensibilidade .NET</span><span class="sxs-lookup"><span data-stu-id="c0385-118">.NET Extensibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0385-119">Desenvolvimento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="c0385-119">Application Development</span></span></p></td>
<td><p><span data-ttu-id="c0385-120">Extensões ISAPI</span><span class="sxs-lookup"><span data-stu-id="c0385-120">ISAPI Extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0385-121">Desenvolvimento do aplicativo</span><span class="sxs-lookup"><span data-stu-id="c0385-121">Application Development</span></span></p></td>
<td><p><span data-ttu-id="c0385-122">Filtros ISAPI</span><span class="sxs-lookup"><span data-stu-id="c0385-122">ISAPI Filters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0385-123">Integridade e Diagnósticos</span><span class="sxs-lookup"><span data-stu-id="c0385-123">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="c0385-124">Ferramentas de log</span><span class="sxs-lookup"><span data-stu-id="c0385-124">Logging Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0385-125">Integridade e Diagnósticos</span><span class="sxs-lookup"><span data-stu-id="c0385-125">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="c0385-126">Rastreamento</span><span class="sxs-lookup"><span data-stu-id="c0385-126">Tracing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0385-127">Segurança</span><span class="sxs-lookup"><span data-stu-id="c0385-127">Security</span></span></p></td>
<td><p><span data-ttu-id="c0385-128">Autenticação básica</span><span class="sxs-lookup"><span data-stu-id="c0385-128">Basic Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0385-129">Segurança</span><span class="sxs-lookup"><span data-stu-id="c0385-129">Security</span></span></p></td>
<td><p><span data-ttu-id="c0385-130">Autenticação do Windows</span><span class="sxs-lookup"><span data-stu-id="c0385-130">Windows Authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0385-131">Ferramentas de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="c0385-131">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="c0385-132">Ferramentas e scripts de gerenciamento IIS</span><span class="sxs-lookup"><span data-stu-id="c0385-132">IIS Management Scripts and Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0385-133">Ferramentas de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="c0385-133">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="c0385-134">Compatibilidade com gerenciamento do IIS 6</span><span class="sxs-lookup"><span data-stu-id="c0385-134">IIS 6 Management Compatibility</span></span></p></td>
</tr>
</tbody>
</table>


<div>

<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="segurança" alt="security" /><span data-ttu-id="c0385-136">Observação de segurança:</span><span class="sxs-lookup"><span data-stu-id="c0385-136">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0385-137">Se você estiver usando o IIS 7,0 em um sistema operacional Windows Server 2008, a instalação do Lync Server desabilitará a autenticação do modo kernel no IIS.</span><span class="sxs-lookup"><span data-stu-id="c0385-137">If you are using IIS 7.0 on a Windows Server 2008 operating system, Lync Server Setup disables kernel mode authentication in IIS.</span></span></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c0385-138">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c0385-138">In This Section</span></span>

  - [<span data-ttu-id="c0385-139">Requisitos de IIS para pools Front-End pools e servidores Standard Edition no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0385-139">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-iis-requirements-for-front-end-pools-and-standard-edition-servers.md)

<span data-ttu-id="c0385-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0385-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

