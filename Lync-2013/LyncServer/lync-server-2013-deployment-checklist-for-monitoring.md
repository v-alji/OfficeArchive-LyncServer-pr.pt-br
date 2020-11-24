---
title: 'Lync Server 2013: Lista de verificação de implantação para monitoramento'
description: 'Lync Server 2013: lista de verificação de implantação para monitoramento.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for monitoring
ms:assetid: 4e798370-277c-4391-84b4-13a972b45ca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204874(v=OCS.15)
ms:contentKeyID: 48184080
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fe3d3293accf6e25c20ae8391f9107ae75fef338
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390103"
---
# <a name="deployment-checklist-for-monitoring-in-lync-server-2013"></a><span data-ttu-id="df13c-103">Lista de verificação de implantação para monitoramento no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df13c-103">Deployment checklist for monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="df13c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="df13c-104">

<span> </span></span></span>

<span data-ttu-id="df13c-105">_**Tópico da última modificação:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="df13c-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="df13c-106">Embora o monitoramento já esteja instalado e ativado em cada servidor front-end, ainda há várias etapas que você deve realizar antes de realmente poder coletar dados de monitoramento do Microsoft Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="df13c-106">Although monitoring is already installed and activated on each Front End server, there are still several steps that you must undertake before you can actually being to collect monitoring data for Microsoft Lync Server 2013.</span></span> <span data-ttu-id="df13c-107">Essas etapas são descritas na seguinte lista de verificação:</span><span class="sxs-lookup"><span data-stu-id="df13c-107">These steps are outlined in the following checklist:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df13c-108">Fase</span><span class="sxs-lookup"><span data-stu-id="df13c-108">Phase</span></span></p></td>
<td><p><span data-ttu-id="df13c-109">Etapas</span><span class="sxs-lookup"><span data-stu-id="df13c-109">Steps</span></span></p></td>
<td><p><span data-ttu-id="df13c-110">Associação de grupo e função</span><span class="sxs-lookup"><span data-stu-id="df13c-110">Role and group membership</span></span></p></td>
<td><p><span data-ttu-id="df13c-111">Documentação</span><span class="sxs-lookup"><span data-stu-id="df13c-111">Documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df13c-112"><strong>Instalar os pré-requisitos de hardware e software</strong></span><span class="sxs-lookup"><span data-stu-id="df13c-112"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="df13c-113">Instale uma versão do Microsoft SQL Server suportada no computador que atuará como armazenamento de dados back-end do monitoramento.</span><span class="sxs-lookup"><span data-stu-id="df13c-113">Install a supported version of Microsoft SQL Server on the computer that will act as the backend data store for monitoring.</span></span></p></td>
<td><p><span data-ttu-id="df13c-114">Usuário do domínio que também é membro do grupo local de administradores.</span><span class="sxs-lookup"><span data-stu-id="df13c-114">Domain user who is also a member of the local administrators group.</span></span></p></td>
<td><p><span data-ttu-id="df13c-115"><a href="lync-server-2013-supported-hardware.md">Hardware com suporte para o Lync Server 2013</a> no guia de suporte</span><span class="sxs-lookup"><span data-stu-id="df13c-115"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability guide</span></span></p>
<p><span data-ttu-id="df13c-116"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Suporte de software e infraestrutura do servidor no Lync Server 2013</a> no guia de suporte</span><span class="sxs-lookup"><span data-stu-id="df13c-116"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability Guide</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df13c-117"><strong>Criar a topologia interna apropriada para dar suporte ao monitoramento</strong></span><span class="sxs-lookup"><span data-stu-id="df13c-117"><strong>Create the appropriate internal topology to support monitoring</strong></span></span></p></td>
<td><p><span data-ttu-id="df13c-118">Use o construtor de topologia do Lync Server 2013 para adicionar bancos de dados de monitoramento à topologia e, em seguida, publicar a topologia atualizada.</span><span class="sxs-lookup"><span data-stu-id="df13c-118">Use Lync Server 2013 Topology Builder to add monitoring databases to the topology, then published the updated topology.</span></span></p></td>
<td><p><span data-ttu-id="df13c-119">Para definir uma topologia, um usuário que seja membro do grupo Usuários local.</span><span class="sxs-lookup"><span data-stu-id="df13c-119">To define a topology, a user who is a member of the local users group.</span></span></p>
<p><span data-ttu-id="df13c-120">Para publicar a topologia, um usuário que seja membro do grupo Administradores de domínio e do grupo RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="df13c-120">To publish the topology, a user who is a member if the domain administrators group and the RTCUniversalServerAdmins group.</span></span></p></td>
<td><p><span data-ttu-id="df13c-121"><a href="lync-server-2013-associating-a-monitoring-store-with-a-front-end-pool.md">Associando um repositório de monitoramento a um pool de front-end no Lync Server 2013</a> no guia de implantação</span><span class="sxs-lookup"><span data-stu-id="df13c-121"><a href="lync-server-2013-associating-a-monitoring-store-with-a-front-end-pool.md">Associating a monitoring store with a Front End pool in Lync Server 2013</a> in the Deployment guide</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df13c-122"><strong>Habilitar a configuração de monitoramento apropriada</strong></span><span class="sxs-lookup"><span data-stu-id="df13c-122"><strong>Enable the appropriate monitoring settings</strong></span></span></p></td>
<td><p><span data-ttu-id="df13c-123">Habilite o monitoramento de registro de detalhes de chamadas (CDR) e/ou Quality of Experience (QoE) nos escopos global e/ou do site.</span><span class="sxs-lookup"><span data-stu-id="df13c-123">Enable call detail recording (CDR) and/or Quality of Experience (QoE) monitoring at the global and/or the site scopes.</span></span></p></td>
<td><p><span data-ttu-id="df13c-124">Um usuário que seja membro do grupo RTCUniversalServerAdmins ou que tenha sido atribuído a uma função RBAC que fornece acesso aos cmdlets CsCdrConfiguration e CsQoEConfiguration.</span><span class="sxs-lookup"><span data-stu-id="df13c-124">A user who is a member of the RTCUniversalServerAdmins group or who has been assigned an RBAC role that provides access to the CsCdrConfiguration and CsQoEConfiguration cmdlets.</span></span></p></td>
<td><p><span data-ttu-id="df13c-125"><a href="lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md">Configurando a gravação de detalhes da chamada e as configurações de qualidade de experiência no Lync Server 2013</a> no guia de operações</span><span class="sxs-lookup"><span data-stu-id="df13c-125"><a href="lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md">Configuring call detail recording and Quality of Experience settings in Lync Server 2013</a> in the Operations guide</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="df13c-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="df13c-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

