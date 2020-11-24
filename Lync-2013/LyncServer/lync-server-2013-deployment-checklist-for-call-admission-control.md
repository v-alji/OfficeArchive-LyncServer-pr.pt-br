---
title: 'Lync Server 2013: Lista de verificação de implantação para controle de admissão de chamada'
description: 'Lync Server 2013: lista de verificação de implantação para controle de admissão de chamadas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for call admission control
ms:assetid: 7e56a169-3e63-44ab-bf28-1fdeb52381c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398631(v=OCS.15)
ms:contentKeyID: 48184621
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea5b16d41228faf01637e7e0d78f5ce56f950a19
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49389703"
---
# <a name="deployment-checklist-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="21e4c-103">Lista de verificação de implantação para controle de admissão de chamada no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21e4c-103">Deployment checklist for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="21e4c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="21e4c-104">

<span> </span></span></span>

<span data-ttu-id="21e4c-105">_**Tópico da última modificação:** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="21e4c-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="21e4c-106">Para planejar efetivamente o controle de admissão de chamadas (CAC), você precisa considerar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="21e4c-106">To plan effectively for call admission control (CAC), you need to consider the following:</span></span>

  - <span data-ttu-id="21e4c-107">Pré-requisitos para a implantação do CAC.</span><span class="sxs-lookup"><span data-stu-id="21e4c-107">Prerequisites for deploying CAC.</span></span>

  - <span data-ttu-id="21e4c-108">Informações necessárias para o CAC e decisões de configuração que você deve fazer antes da implantação.</span><span class="sxs-lookup"><span data-stu-id="21e4c-108">Information required for CAC and configuration decisions that you must make in advance of deployment.</span></span>

<div>

## <a name="deployment-prerequisites-for-call-admission-control"></a><span data-ttu-id="21e4c-109">Pré-requisitos de implantação para controle de admissão de chamadas</span><span class="sxs-lookup"><span data-stu-id="21e4c-109">Deployment Prerequisites for Call Admission Control</span></span>

<span data-ttu-id="21e4c-110">Antes de implantar o controle de admissão de chamadas, você já deve ter implantado seus servidores internos do Lync Server 2013, incluindo um pool de front-ends ou um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="21e4c-110">Before you deploy call admission control, you must already have deployed your Lync Server 2013 internal servers, including either a Front End pool or a Standard Edition server.</span></span>

</div>

<div>

## <a name="information-requirements-for-call-admission-control"></a><span data-ttu-id="21e4c-111">Requisitos de informações para controle de admissão de chamadas</span><span class="sxs-lookup"><span data-stu-id="21e4c-111">Information Requirements for Call Admission Control</span></span>

<span data-ttu-id="21e4c-112">A tabela a seguir resume as informações necessárias para implantar o controle de admissão de chamadas.</span><span class="sxs-lookup"><span data-stu-id="21e4c-112">The following table summarizes the required information for deploying call admission control.</span></span>

### <a name="information-requirements-for-call-admission-control-deployment"></a><span data-ttu-id="21e4c-113">Requisitos de informações para a implantação do controle de admissão de chamadas</span><span class="sxs-lookup"><span data-stu-id="21e4c-113">Information Requirements for Call Admission Control Deployment</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="21e4c-114">Informações</span><span class="sxs-lookup"><span data-stu-id="21e4c-114">Information</span></span></th>
<th><span data-ttu-id="21e4c-115">Resumo das informações necessárias</span><span class="sxs-lookup"><span data-stu-id="21e4c-115">Summary of Information Required</span></span></th>
<th><span data-ttu-id="21e4c-116">Documentação</span><span class="sxs-lookup"><span data-stu-id="21e4c-116">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21e4c-117">Recursos do Lync Server exigidos pela sua organização</span><span class="sxs-lookup"><span data-stu-id="21e4c-117">Lync Server capabilities required by your organization</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="21e4c-118">Recursos a serem suportados pela sua organização</span><span class="sxs-lookup"><span data-stu-id="21e4c-118">Capabilities to be supported by your organization</span></span></p></li>
<li><p><span data-ttu-id="21e4c-119">Recursos a serem habilitados para usuários individuais</span><span class="sxs-lookup"><span data-stu-id="21e4c-119">Capabilities to be enabled for individual users</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="21e4c-120"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Definindo seus requisitos de controle de admissão de chamadas no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21e4c-120"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e4c-121">Topologias e componentes a serem implantados</span><span class="sxs-lookup"><span data-stu-id="21e4c-121">Topologies and components to be deployed</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="21e4c-122">Os componentes relacionados ao CAC são instalados automaticamente como parte do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21e4c-122">CAC related components are automatically installed as part of Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="21e4c-123"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Definindo seus requisitos de controle de admissão de chamadas no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21e4c-123"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e4c-124">Requisitos do sistema</span><span class="sxs-lookup"><span data-stu-id="21e4c-124">System requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="21e4c-125">Requisitos de hardware</span><span class="sxs-lookup"><span data-stu-id="21e4c-125">Hardware requirements</span></span></p></li>
<li><p><span data-ttu-id="21e4c-126">Requisitos de software</span><span class="sxs-lookup"><span data-stu-id="21e4c-126">Software requirements</span></span></p></li>
<li><p><span data-ttu-id="21e4c-127">Requisitos de colocação</span><span class="sxs-lookup"><span data-stu-id="21e4c-127">Collocation requirements</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="21e4c-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determinando seus requisitos de sistema para Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21e4c-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e4c-129">Requisitos de infraestrutura</span><span class="sxs-lookup"><span data-stu-id="21e4c-129">Infrastructure requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="21e4c-130">Nenhuma necessidade de infraestrutura específica é necessária para o CAC</span><span class="sxs-lookup"><span data-stu-id="21e4c-130">No specific infrastructure requirements are necessary for CAC</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="21e4c-131"><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Requisitos de infraestrutura para controle de admissão de chamada no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21e4c-131"><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Infrastructure requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e4c-132">Requisitos de interface de rede</span><span class="sxs-lookup"><span data-stu-id="21e4c-132">Network interface requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="21e4c-133">Informações de interface interna e externa</span><span class="sxs-lookup"><span data-stu-id="21e4c-133">Internal and external interface information</span></span></p></li>
<li><p><span data-ttu-id="21e4c-134">Informações de roteamento (incluindo informações sobre o blog NextHop em <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a> , canal de resposta do cliente da equipe do Microsoft Lync Server)</span><span class="sxs-lookup"><span data-stu-id="21e4c-134">Routing information (including information on the NextHop blog at <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a>, Microsoft Lync Server team’s customer response channel)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="21e4c-135"><a href="lync-server-2013-deploying-external-user-access.md">Implantação de acesso do usuário externo no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21e4c-135"><a href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e4c-136">Estratégia de implantação</span><span class="sxs-lookup"><span data-stu-id="21e4c-136">Deployment strategy</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="21e4c-137">Sequência de implantação</span><span class="sxs-lookup"><span data-stu-id="21e4c-137">Deployment sequence</span></span></p></li>
<li><p><span data-ttu-id="21e4c-138">Grupo de trabalho ou domínio</span><span class="sxs-lookup"><span data-stu-id="21e4c-138">Workgroup or domain</span></span></p></li>
<li><p><span data-ttu-id="21e4c-139">Segurança</span><span class="sxs-lookup"><span data-stu-id="21e4c-139">Security</span></span></p></li>
<li><p><span data-ttu-id="21e4c-140">Monitoramento e auditoria</span><span class="sxs-lookup"><span data-stu-id="21e4c-140">Monitoring and auditing</span></span></p></li>
<li><p><span data-ttu-id="21e4c-141">Considerações de hardware</span><span class="sxs-lookup"><span data-stu-id="21e4c-141">Hardware considerations</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="21e4c-142"><a href="lync-server-2013-best-practices-for-call-admission-control.md">Práticas recomendadas para controle de admissão de chamada no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21e4c-142"><a href="lync-server-2013-best-practices-for-call-admission-control.md">Best practices for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e4c-143">Processo de implantação</span><span class="sxs-lookup"><span data-stu-id="21e4c-143">Deployment process</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="21e4c-144">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="21e4c-144">Prerequisites</span></span></p></li>
<li><p><span data-ttu-id="21e4c-145">Requisitos de informações</span><span class="sxs-lookup"><span data-stu-id="21e4c-145">Information requirements</span></span></p></li>
<li><p><span data-ttu-id="21e4c-146">Processo e procedimentos</span><span class="sxs-lookup"><span data-stu-id="21e4c-146">Process and procedures</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="21e4c-147"><a href="lync-server-2013-configure-call-admission-control.md">Configurar o controle de admissão de chamadas no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="21e4c-147"><a href="lync-server-2013-configure-call-admission-control.md">Configure call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="21e4c-148">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="21e4c-148">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

