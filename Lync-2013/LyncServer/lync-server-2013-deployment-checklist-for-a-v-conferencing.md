---
title: Lista de verificação de implantação do Lync Server 2013 para conferência A/V
description: Lista de verificação de implantação do Lync Server 2013 para conferência A/V.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for A/V conferencing
ms:assetid: 6d47426f-6559-407b-9ac1-2453f0b7a2a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619183(v=OCS.15)
ms:contentKeyID: 49733684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9a4584172ed4c01eb163ea51aa4f62c2ce75185
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429747"
---
# <a name="deployment-checklist-for-av-conferencing-in-lync-server-2013"></a><span data-ttu-id="d0f82-103">Lista de verificação de implantação para conferência A/V no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f82-103">Deployment checklist for A/V conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d0f82-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d0f82-104">

<span> </span></span></span>

<span data-ttu-id="d0f82-105">_**Tópico da última modificação:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="d0f82-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="d0f82-106">Assim como com a implantação de outros componentes do Lync Server 2013, A implantação de uma conferência A/V requer que você use o construtor de topologias para criar e publicar uma topologia que incorpora conferências.</span><span class="sxs-lookup"><span data-stu-id="d0f82-106">As with deployment of your other Lync Server 2013 components, deployment of A/V conferencing requires that you use Topology Builder to create and publish a topology that incorporates conferencing.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="d0f82-107">Sequência de implantação</span><span class="sxs-lookup"><span data-stu-id="d0f82-107">Deployment Sequence</span></span>

<span data-ttu-id="d0f82-108">Você pode implantar conferências ao mesmo tempo em que implantar a sua topologia inicial ou depois de implantar pelo menos um pool de front-end ou um servidor Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d0f82-108">You can deploy conferencing at the same time that you deploy your initial topology or after you have deployed at least one Front End pool or Standard Edition server.</span></span>

</div>

<div>

## <a name="conferencing-deployment-process"></a><span data-ttu-id="d0f82-109">Processo de implantação de conferência</span><span class="sxs-lookup"><span data-stu-id="d0f82-109">Conferencing Deployment Process</span></span>

<span data-ttu-id="d0f82-110">A tabela a seguir fornece uma visão geral das etapas necessárias para implantar a conferência em uma topologia existente.</span><span class="sxs-lookup"><span data-stu-id="d0f82-110">The following table provides an overview of the steps required to deploy conferencing into an existing topology.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0f82-111">Fase</span><span class="sxs-lookup"><span data-stu-id="d0f82-111">Phase</span></span></th>
<th><span data-ttu-id="d0f82-112">Etapas</span><span class="sxs-lookup"><span data-stu-id="d0f82-112">Steps</span></span></th>
<th><span data-ttu-id="d0f82-113">Funções e associações de grupo</span><span class="sxs-lookup"><span data-stu-id="d0f82-113">Roles and group memberships</span></span></th>
<th><span data-ttu-id="d0f82-114">Documentação</span><span class="sxs-lookup"><span data-stu-id="d0f82-114">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0f82-115"><strong>Instalar pré-requisitos de hardware e software</strong></span><span class="sxs-lookup"><span data-stu-id="d0f82-115"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="d0f82-116">A conferência é executada em servidores front-end de um pool de front-end e servidores Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="d0f82-116">Conferencing runs on Front End Servers of a Front End pool and Standard Edition servers.</span></span> <span data-ttu-id="d0f82-117">Não há requisitos adicionais de hardware ou software além daqueles necessários para instalar esses servidores.</span><span class="sxs-lookup"><span data-stu-id="d0f82-117">It has no additional hardware or software requirements beyond what is required to install those servers.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="d0f82-118">O Lync Server 2013 usa o Office Web Apps e o Office Web Apps Server para lidar com o compartilhamento e a renderização de apresentações do PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="d0f82-118">Lync Server 2013 uses Office Web Apps and the Office Web Apps Server to handle sharing and rendering of PowerPoint presentations.</span></span> <span data-ttu-id="d0f82-119">Para obter detalhes sobre como instalar e configurar o Office Web Apps Server, consulte <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Configurando a integração com o Office Web Apps Server e o Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d0f82-119">For details about installing and configuring the Office Web Apps Server, see <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Configuring integration with Office Web Apps Server and Lync Server 2013</A>.</span></span>


</div></td>
<td><p><span data-ttu-id="d0f82-120">Domínio do usuário que é membro do grupo local de Administradores</span><span class="sxs-lookup"><span data-stu-id="d0f82-120">Domain user who is a member of the local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="d0f82-121"><a href="lync-server-2013-supported-hardware.md">Hardware com suporte para o Lync Server 2013</a> na documentação de suporte</span><span class="sxs-lookup"><span data-stu-id="d0f82-121"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="d0f82-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Suporte de software e infraestrutura do servidor no Lync Server 2013</a> na documentação de suporte</span><span class="sxs-lookup"><span data-stu-id="d0f82-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="d0f82-123"><a href="lync-server-2013-determining-your-system-requirements.md">Determinação dos requisitos do sistema para o Lync Server 2013</a> na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="d0f82-123"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="d0f82-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Requisitos técnicos para arquivamento no Lync Server 2013</a> na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="d0f82-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Technical requirements for Archiving in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0f82-125"><strong>Crie a topologia interna apropriada para dar suporte à conferência</strong></span><span class="sxs-lookup"><span data-stu-id="d0f82-125"><strong>Create the appropriate internal topology to support conferencing</strong></span></span></p></td>
<td><p><span data-ttu-id="d0f82-126">Execute o construtor de topologias para adicionar conferências à topologia e, em seguida, publique a topologia.</span><span class="sxs-lookup"><span data-stu-id="d0f82-126">Run Topology Builder to add conferencing to the topology, and then publish the topology.</span></span></p></td>
<td><p><span data-ttu-id="d0f82-127">Para definir a topologia, uma conta que é membro do grupo local de Usuários</span><span class="sxs-lookup"><span data-stu-id="d0f82-127">To define a topology, an account that is a member of the local Users group</span></span></p>
<p><span data-ttu-id="d0f82-128">Para publicar a topologia, uma conta que é membro do grupo Domain admins e do grupo RTCUniversalServerAdmins e que tem permissões de controle total (ler/gravar/modificar) no compartilhamento de arquivos a ser usado para o repositório de arquivos do Lync Server 2013 (para que o construtor de topologias possa configurar as DACLs necessárias)</span><span class="sxs-lookup"><span data-stu-id="d0f82-128">To publish the topology, an account that is a member of the Domain Admins group and RTCUniversalServerAdmins group, and that has full control permissions (read/write/modify) on the file share to be used for the Lync Server 2013 file store (so that Topology Builder can configure the required DACLs)</span></span></p></td>
<td><p><span data-ttu-id="d0f82-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Defina e configure uma topologia no construtor de topologias para o Lync Server 2013</a> na documentação de implantação.</span><span class="sxs-lookup"><span data-stu-id="d0f82-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Define and configure a topology in Topology Builder for Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0f82-130"><strong>Configurar políticas de conferência e suporte</strong></span><span class="sxs-lookup"><span data-stu-id="d0f82-130"><strong>Configure conferencing policies and support</strong></span></span></p></td>
<td><p><span data-ttu-id="d0f82-131">Use o painel de controle do Lync Server 2013 ou o Shell de gerenciamento do Lync Server para definir as configurações de conferência.</span><span class="sxs-lookup"><span data-stu-id="d0f82-131">Use the Lync Server 2013 Control Panel or Lync Server Management Shell to configure conferencing settings.</span></span></p></td>
<td><p><span data-ttu-id="d0f82-132">Grupo RTCUniversalServerAdmins (somente Windows PowerShell) ou atribuir usuários à função [] ou CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="d0f82-132">RTCUniversalServerAdmins group (Windows PowerShell only) or assign users to the [] or CSAdministrator role</span></span></p></td>
<td><p><span data-ttu-id="d0f82-133"><a href="lync-server-2013-conferencing-policies.md">Políticas de conferência no Lync Server 2013</a> na documentação de operações.</span><span class="sxs-lookup"><span data-stu-id="d0f82-133"><a href="lync-server-2013-conferencing-policies.md">Conferencing policies in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d0f82-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0f82-134">See Also</span></span>


[<span data-ttu-id="d0f82-135">Visão geral de conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f82-135">Overview of conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-conferencing.md)  
[<span data-ttu-id="d0f82-136">Definindo seus requisitos para conferência no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0f82-136">Defining your requirements for conferencing in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-conferencing.md)  
  

<span data-ttu-id="d0f82-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d0f82-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

