---
title: 'Lync Server 2013: Compreendendo os requisitos de firewall para Servidor SQL'
description: 'Lync Server 2013: compreendendo os requisitos de firewall do SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding firewall requirements for SQL Server
ms:assetid: 31d7df2c-589f-465e-be74-cf6767db190d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425818(v=OCS.15)
ms:contentKeyID: 48183781
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c434474b36ced0fe64b9398f7d0e6136ff523a93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390217"
---
# <a name="understanding-firewall-requirements-for-sql-server-with-lync-server-2013"></a><span data-ttu-id="f0a4b-103">Compreendendo os requisitos de firewall para Servidor SQL com Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0a4b-103">Understanding firewall requirements for SQL Server with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f0a4b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f0a4b-104">

<span> </span></span></span>

<span data-ttu-id="f0a4b-105">_**Tópico da última modificação:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="f0a4b-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="f0a4b-106">Para uma implantação de edição padrão, as exceções de firewall são criadas automaticamente durante a instalação do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-106">For a Standard Edition deployment, firewall exceptions are created automatically during Lync Server 2013 Setup.</span></span> <span data-ttu-id="f0a4b-107">No entanto, para implantações do Enterprise Edition, você deve configurar as exceções de firewall manualmente no servidor back-end do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-107">However, for Enterprise Edition deployments, you must configure the firewall exceptions manually on the SQL Server Back End Server.</span></span> <span data-ttu-id="f0a4b-108">O protocolo TCP/IP permite que uma determinada porta seja usada uma vez para um determinado endereço IP.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-108">The TCP/IP protocol allows for a given port to be used once for a given IP address.</span></span> <span data-ttu-id="f0a4b-109">Isso significa que, para o servidor baseado no SQL Server, você pode atribuir à instância de banco de dados padrão a porta TCP 1433.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-109">This means that for the SQL Server-based server you can assign the default database instance the default TCP port 1433.</span></span> <span data-ttu-id="f0a4b-110">Para quaisquer outros casos, você precisará usar o Gerenciador de configuração do SQL Server para atribuir portas exclusivas e não utilizadas.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-110">For any other instances you will need to use the SQL Server Configuration Manager to assign unique and unused ports.</span></span> <span data-ttu-id="f0a4b-111">Este tópico aborda:</span><span class="sxs-lookup"><span data-stu-id="f0a4b-111">This topic covers:</span></span>

  - <span data-ttu-id="f0a4b-112">Requisitos para uma exceção de firewall ao usar a instância padrão</span><span class="sxs-lookup"><span data-stu-id="f0a4b-112">Requirements for a firewall exception when using the default instance</span></span>

  - <span data-ttu-id="f0a4b-113">Requisitos para uma exceção de firewall para o serviço do navegador do SQL Server</span><span class="sxs-lookup"><span data-stu-id="f0a4b-113">Requirements for a firewall exception for the SQL Server Browser service</span></span>

  - <span data-ttu-id="f0a4b-114">Requisitos para portas de escuta estática ao usar instâncias nomeadas</span><span class="sxs-lookup"><span data-stu-id="f0a4b-114">Requirements for static listening ports when using named instances</span></span>

<div>

## <a name="requirements-for-a-firewall-exception-when-using-the-default-instance"></a><span data-ttu-id="f0a4b-115">Requisitos para uma exceção de firewall ao usar a instância padrão</span><span class="sxs-lookup"><span data-stu-id="f0a4b-115">Requirements for a Firewall Exception When Using the Default Instance</span></span>

<span data-ttu-id="f0a4b-116">Se você estiver usando a instância padrão do SQL Server para qualquer banco de dados ao implantar o Lync Server 2013, os seguintes requisitos de regra de firewall são usados para ajudar a garantir a comunicação do pool de front-ends para a instância padrão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-116">If you are using the SQL Server default instance for any database when deploying Lync Server 2013, the following firewall rule requirements are used to help ensure communication from the Front End pool to the SQL Server default instance.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0a4b-117">Protocolo</span><span class="sxs-lookup"><span data-stu-id="f0a4b-117">Protocol</span></span></th>
<th><span data-ttu-id="f0a4b-118">Porta</span><span class="sxs-lookup"><span data-stu-id="f0a4b-118">Port</span></span></th>
<th><span data-ttu-id="f0a4b-119">Direção</span><span class="sxs-lookup"><span data-stu-id="f0a4b-119">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0a4b-120">TCP</span><span class="sxs-lookup"><span data-stu-id="f0a4b-120">TCP</span></span></p></td>
<td><p><span data-ttu-id="f0a4b-121">1433</span><span class="sxs-lookup"><span data-stu-id="f0a4b-121">1433</span></span></p></td>
<td><p><span data-ttu-id="f0a4b-122">Entrada do SQL Server</span><span class="sxs-lookup"><span data-stu-id="f0a4b-122">Inbound to SQL Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-a-firewall-exception-for-the-sql-server-browser-service"></a><span data-ttu-id="f0a4b-123">Requisitos para uma exceção de firewall para o serviço do navegador do SQL Server</span><span class="sxs-lookup"><span data-stu-id="f0a4b-123">Requirements for a Firewall Exception for the SQL Server Browser Service</span></span>

<span data-ttu-id="f0a4b-124">O serviço de navegador do SQL Server localizará instâncias de banco de dados e comunicará a porta que a instância (nomeada ou padrão) está configurada para usar.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-124">The SQL Server Browser service will locate database instances and communicate the port that the instance (named or default) is configured to use.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0a4b-125">Protocolo</span><span class="sxs-lookup"><span data-stu-id="f0a4b-125">Protocol</span></span></th>
<th><span data-ttu-id="f0a4b-126">Porta</span><span class="sxs-lookup"><span data-stu-id="f0a4b-126">Port</span></span></th>
<th><span data-ttu-id="f0a4b-127">Direção</span><span class="sxs-lookup"><span data-stu-id="f0a4b-127">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0a4b-128">UDP</span><span class="sxs-lookup"><span data-stu-id="f0a4b-128">UDP</span></span></p></td>
<td><p><span data-ttu-id="f0a4b-129">1434</span><span class="sxs-lookup"><span data-stu-id="f0a4b-129">1434</span></span></p></td>
<td><p><span data-ttu-id="f0a4b-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0a4b-130">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-static-listening-ports-when-using-named-instances"></a><span data-ttu-id="f0a4b-131">Requisitos para portas de escuta estática ao usar instâncias nomeadas</span><span class="sxs-lookup"><span data-stu-id="f0a4b-131">Requirements for Static Listening Ports When Using Named Instances</span></span>

<span data-ttu-id="f0a4b-132">Ao usar instâncias nomeadas na configuração do SQL Server para bancos de dados que ofereçam suporte ao Lync Server 2013, você configura portas estáticas usando o Gerenciador de configuração do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-132">When using named instances in the SQL Server configuration for databases supporting Lync Server 2013, you configure static ports by using SQL Server Configuration Manager.</span></span> <span data-ttu-id="f0a4b-133">Após a atribuição das portas estáticas a cada instância nomeada, você cria exceções para cada porta estática do firewall.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-133">After the static ports have been assigned to each named instance, you create exceptions for each static port in the firewall.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0a4b-134">Protocolo</span><span class="sxs-lookup"><span data-stu-id="f0a4b-134">Protocol</span></span></th>
<th><span data-ttu-id="f0a4b-135">Porta</span><span class="sxs-lookup"><span data-stu-id="f0a4b-135">Port</span></span></th>
<th><span data-ttu-id="f0a4b-136">Direção</span><span class="sxs-lookup"><span data-stu-id="f0a4b-136">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0a4b-137">TCP</span><span class="sxs-lookup"><span data-stu-id="f0a4b-137">TCP</span></span></p></td>
<td><p><span data-ttu-id="f0a4b-138">Definido estaticamente</span><span class="sxs-lookup"><span data-stu-id="f0a4b-138">Statically defined</span></span></p></td>
<td><p><span data-ttu-id="f0a4b-139">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0a4b-139">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="sql-server-documentation"></a><span data-ttu-id="f0a4b-140">Documentação do SQL Server</span><span class="sxs-lookup"><span data-stu-id="f0a4b-140">SQL Server Documentation</span></span>

<span data-ttu-id="f0a4b-141">A documentação do Microsoft SQL Server 2012 fornece orientações detalhadas sobre como configurar o acesso do firewall para bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="f0a4b-141">Microsoft SQL Server 2012 documentation provides detailed guidance on how to configure firewall access for databases.</span></span> <span data-ttu-id="f0a4b-142">Para obter detalhes sobre o Microsoft SQL Server 2012, consulte "Configurando o Firewall do Windows para permitir o acesso ao SQL Server" em [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031) .</span><span class="sxs-lookup"><span data-stu-id="f0a4b-142">For details about Microsoft SQL Server 2012, see “Configuring the Windows Firewall to Allow SQL Server Access” at [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031).</span></span>

<span data-ttu-id="f0a4b-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f0a4b-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

