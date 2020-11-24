---
title: 'Lync Server 2013: Lista de verificação de implantação para o Servidor de Chat Persistente'
description: 'Lync Server 2013: lista de verificação de implantação para servidor de chat persistente.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for Persistent Chat Server
ms:assetid: b1108f8f-88a2-4660-8086-d25ba76f7239
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412851(v=OCS.15)
ms:contentKeyID: 48185155
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28d96da5e2961634e6a81450796e5d1ae3426819
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390102"
---
# <a name="deployment-checklist-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="be891-103">Lista de verificação de implantação para o Servidor de Chat Persistente no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be891-103">Deployment checklist for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be891-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be891-104">

<span> </span></span></span>

<span data-ttu-id="be891-105">_**Tópico da última modificação:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="be891-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="be891-106">A implantação do Lync Server 2013, servidor de chat persistente exige que você o implante na sequência correta e conclua todas as etapas de implantação necessárias.</span><span class="sxs-lookup"><span data-stu-id="be891-106">Deployment of Lync Server 2013, Persistent Chat Server requires that you deploy it in the correct sequence and that you complete all required deployment steps.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="be891-107">Sequência de implantação</span><span class="sxs-lookup"><span data-stu-id="be891-107">Deployment Sequence</span></span>

<span data-ttu-id="be891-108">Você pode implantar o servidor de chat persistente após implantar a topologia inicial, incluindo pelo menos um Lync Server 2013, um pool de front-end ou um servidor do Lync Server 2013, Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="be891-108">You can deploy Persistent Chat Server after you deploy your initial topology, including at least one Lync Server 2013, Front End pool or one Lync Server 2013, Standard Edition server.</span></span> <span data-ttu-id="be891-109">Este tópico descreve como implantar o servidor de chat persistente adicionando-o a uma implantação existente.</span><span class="sxs-lookup"><span data-stu-id="be891-109">This topic describes how to deploy Persistent Chat Server by adding it to an existing deployment.</span></span>

</div>

<div>

## <a name="deployment-process"></a><span data-ttu-id="be891-110">Processo de implantação</span><span class="sxs-lookup"><span data-stu-id="be891-110">Deployment Process</span></span>

<span data-ttu-id="be891-111">A tabela a seguir lista as etapas básicas para implantar o servidor de chat persistente e fornece links para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="be891-111">The following table lists the basic steps to deploy Persistent Chat Server and provides links for more details.</span></span>

### <a name="persistent-chat-server-deployment-process"></a><span data-ttu-id="be891-112">Processo de implantação do servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="be891-112">Persistent Chat Server Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be891-113">Tarefa</span><span class="sxs-lookup"><span data-stu-id="be891-113">Task</span></span></th>
<th><span data-ttu-id="be891-114">Etapas</span><span class="sxs-lookup"><span data-stu-id="be891-114">Steps</span></span></th>
<th><span data-ttu-id="be891-115">Funções exigidas e associações em grupo</span><span class="sxs-lookup"><span data-stu-id="be891-115">Required roles and group memberships</span></span></th>
<th><span data-ttu-id="be891-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="be891-116">Related topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be891-117"><strong>Instalar pré-requisitos de hardware e software</strong></span><span class="sxs-lookup"><span data-stu-id="be891-117"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="be891-118">No hardware que atender aos requisitos do sistema, instale o seguinte:</span><span class="sxs-lookup"><span data-stu-id="be891-118">On hardware that meets system requirements, install the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="be891-119">Nos servidores de front-end do servidor de chat persistente:</span><span class="sxs-lookup"><span data-stu-id="be891-119">On the Persistent Chat Server Front End Servers:</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="be891-120">Um sistema operacional que atenda aos requisitos do sistema</span><span class="sxs-lookup"><span data-stu-id="be891-120">An operating system that meets system requirements</span></span></p></li>
<li><p><span data-ttu-id="be891-121">Pré-requisitos de software para computadores que executam o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be891-121">Software prerequisites for computers running Lync Server 2013</span></span></p></li>
<li><p><span data-ttu-id="be891-122">SQL Server no servidor que hospedará o banco de dados persistente do servidor de chat</span><span class="sxs-lookup"><span data-stu-id="be891-122">SQL Server on the server that will host Persistent Chat Server database</span></span></p></li>
</ul>
<p><span data-ttu-id="be891-123">Se for necessário conformidade com o servidor de chat persistente:</span><span class="sxs-lookup"><span data-stu-id="be891-123">If Persistent Chat Server compliance is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="be891-124">SQL Server no servidor que hospedará o banco de dados de conformidade do servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="be891-124">SQL Server on the server that will host Persistent Chat Server compliance database</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="be891-125">Qualquer usuário que seja membro do grupo Administradores locais.</span><span class="sxs-lookup"><span data-stu-id="be891-125">Any user who is a member of the local Administrators group.</span></span></p></td>
<td><p><span data-ttu-id="be891-126"><a href="lync-server-2013-supported-hardware.md">Hardware com suporte para o Lync Server 2013</a> na documentação de suporte</span><span class="sxs-lookup"><span data-stu-id="be891-126"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="be891-127"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Suporte de software e infraestrutura do servidor no Lync Server 2013</a> na documentação de suporte</span><span class="sxs-lookup"><span data-stu-id="be891-127"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="be891-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determinando seus requisitos de sistema para Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="be891-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="be891-129"><a href="lync-server-2013-technical-requirements-for-persistent-chat-server.md">Requisitos técnicos para servidor de chat persistente no Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="be891-129"><a href="lync-server-2013-technical-requirements-for-persistent-chat-server.md">Technical requirements for Persistent Chat Server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be891-130"><strong>Criar a topologia interna apropriada para dar suporte a servidor de chat persistente (e, opcionalmente, conformidade de chat persistente)</strong></span><span class="sxs-lookup"><span data-stu-id="be891-130"><strong>Create the appropriate internal topology to support Persistent Chat Server (and optionally, Persistent Chat compliance)</strong></span></span></p></td>
<td><p><span data-ttu-id="be891-131">Execute o construtor de topologias para adicionar um pool de servidores de chat persistentes à sua topologia:</span><span class="sxs-lookup"><span data-stu-id="be891-131">Run Topology Builder to add a Persistent Chat Server pool to your topology:</span></span></p>
<ul>
<li><p><span data-ttu-id="be891-132">Adicionar componentes persistentes do servidor de chat à topologia</span><span class="sxs-lookup"><span data-stu-id="be891-132">Add Persistent Chat Server components to the topology</span></span></p></li>
<li><p><span data-ttu-id="be891-133">Criar um banco de dados SQL Server para o repositório persistente do servidor de chat (e um SQL Server de backup para recuperação de desastres)</span><span class="sxs-lookup"><span data-stu-id="be891-133">Create a SQL Server database for the Persistent Chat Server store (and a backup SQL Server for disaster recovery)</span></span></p></li>
<li><p><span data-ttu-id="be891-134">Definir um novo repositório de arquivos do Lync ou usar um repositório de arquivos existente do Lync para arquivos persistentes do servidor de chat</span><span class="sxs-lookup"><span data-stu-id="be891-134">Define a new Lync File Store or use an existing Lync File Store for Persistent Chat Server files</span></span></p></li>
<li><p><span data-ttu-id="be891-135">Associar o pool do Lync Server 2013 que pode rotear solicitações para este pool do servidor de chat persistente</span><span class="sxs-lookup"><span data-stu-id="be891-135">Associate the Lync Server 2013 pool that can route requests to this Persistent Chat Server pool</span></span></p></li>
</ul>
<p><span data-ttu-id="be891-136">Se a conformidade com Chat Persistente for necessária:</span><span class="sxs-lookup"><span data-stu-id="be891-136">If Persistent Chat compliance is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="be891-137">Adicionar repositório de conformidade de chat persistente</span><span class="sxs-lookup"><span data-stu-id="be891-137">Add Persistent Chat Compliance Store</span></span></p></li>
<li><p><span data-ttu-id="be891-138">Clique na caixa de seleção definição do pool de servidores de chat persistentes para habilitar a conformidade</span><span class="sxs-lookup"><span data-stu-id="be891-138">Click the Persistent Chat Server pool definition check box for enabling compliance</span></span></p></li>
<li><p><span data-ttu-id="be891-139">Publicar a topologia</span><span class="sxs-lookup"><span data-stu-id="be891-139">Publish the topology</span></span></p></li>
</ul>
<p><span data-ttu-id="be891-140">Se você instalar o servidor de chat persistente na edição Standard, o nome de domínio totalmente qualificado (FQDN) do pool do servidor de chat persistente deve corresponder ao servidor Standard Edition e os bancos de dados do SQL Server são posicionados na instância do SQL Server Express no servidor Standard Edition</span><span class="sxs-lookup"><span data-stu-id="be891-140">If you install Persistent Chat Server on Standard Edition, the fully qualified domain name (FQDN) of the Persistent Chat Server pool must match the Standard Edition server, and the SQL Server databases are collocated on the SQL Server Express instance on the Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="be891-141">Para definir uma topologia, uma canta membro do grupo de usuários local.</span><span class="sxs-lookup"><span data-stu-id="be891-141">To define a topology, an account that is a member of the local Users group.</span></span></p>
<p><span data-ttu-id="be891-142">Para publicar a topologia, uma conta que seja membro do grupo Domain admins e do grupo RTCUniversalServerAdmins e o usuário também deve ter permissões de controle total (ler/gravar/modificar) no repositório de arquivos do Lync para arquivos de servidor de chat persistente (para que o construtor de topologias possa configurar as DACLs necessárias).</span><span class="sxs-lookup"><span data-stu-id="be891-142">To publish the topology, an account that is a member of the Domain Admins group and RTCUniversalServerAdmins group, and the user should also have full control permissions (read/write/modify) on the Lync File Store for Persistent Chat Server files (so that Topology Builder can configure the required DACLs).</span></span></p></td>
<td><p><span data-ttu-id="be891-143"><a href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Adicionar um servidor de chat persistente à sua implantação no Lync Server 2013</a> na documentação de implantação</span><span class="sxs-lookup"><span data-stu-id="be891-143"><a href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">Adding Persistent Chat Server to your deployment in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be891-144"><strong>Implantar Servidor de Chat Persistente</strong></span><span class="sxs-lookup"><span data-stu-id="be891-144"><strong>Deploy Persistent Chat Server</strong></span></span></p></td>
<td><p><span data-ttu-id="be891-145">Execute a instalação do Lync Server em todos os computadores que executam o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="be891-145">Run the Lync Server setup on all the computers running Persistent Chat Server.</span></span> <span data-ttu-id="be891-146">A configuração do servidor de chat persistente está integrada ao assistente de implantação do Lync Server 2013 que fornece as instruções a seguir:</span><span class="sxs-lookup"><span data-stu-id="be891-146">The Persistent Chat Server setup is integrated into the Lync Server 2013 Deployment wizard that provides the following instructions:</span></span></p>
<ul>
<li><p><span data-ttu-id="be891-147">Implantar repositório de gerenciamento local</span><span class="sxs-lookup"><span data-stu-id="be891-147">Deploy local management store</span></span></p></li>
<li><p><span data-ttu-id="be891-148">Instalar serviços persistentes do servidor de chat</span><span class="sxs-lookup"><span data-stu-id="be891-148">Install Persistent Chat Server services</span></span></p></li>
<li><p><span data-ttu-id="be891-149">Solicitar e assinar certificados</span><span class="sxs-lookup"><span data-stu-id="be891-149">Request and assign certificates</span></span></p></li>
<li><p><span data-ttu-id="be891-150">Executar e iniciar os serviços</span><span class="sxs-lookup"><span data-stu-id="be891-150">Run and start the services</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="be891-151">Qualquer usuário que seja membro do grupo Administradores locais.</span><span class="sxs-lookup"><span data-stu-id="be891-151">Any user who is a member of the local Administrators group.</span></span></p></td>
<td><p><span data-ttu-id="be891-152"><a href="lync-server-2013-deploying-persistent-chat-server.md">Implantando o servidor de chat persistente no Lync Server 2013</a> na documentação de implantação</span><span class="sxs-lookup"><span data-stu-id="be891-152"><a href="lync-server-2013-deploying-persistent-chat-server.md">Deploying Persistent Chat Server in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be891-153"><strong>Criar um administrador de Chat Persistente</strong></span><span class="sxs-lookup"><span data-stu-id="be891-153"><strong>Create a Persistent Chat administrator</strong></span></span></p></td>
<td><p><span data-ttu-id="be891-154">Adicionar usuários ao grupo de segurança CsPersistentChatAdministrator.</span><span class="sxs-lookup"><span data-stu-id="be891-154">Add users to the CsPersistentChatAdministrator security group.</span></span></p></td>
<td><p><span data-ttu-id="be891-155">Qualquer usuário que seja membro dos administradores de domínio.</span><span class="sxs-lookup"><span data-stu-id="be891-155">Any user who is a member of domain administrators.</span></span></p></td>
<td><p><span data-ttu-id="be891-156"><a href="lync-server-2013-adding-a-persistent-chat-administrator.md">Adicionar um administrador de chat persistente no Lync Server 2013</a> na documentação de implantação</span><span class="sxs-lookup"><span data-stu-id="be891-156"><a href="lync-server-2013-adding-a-persistent-chat-administrator.md">Adding a Persistent Chat administrator in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be891-157"><strong>Configurar o Servidor de Chat Persistente</strong></span><span class="sxs-lookup"><span data-stu-id="be891-157"><strong>Configure Persistent Chat Server</strong></span></span></p></td>
<td><p><span data-ttu-id="be891-158">Configurar usuários:</span><span class="sxs-lookup"><span data-stu-id="be891-158">Configure users:</span></span></p>
<ul>
<li><p><span data-ttu-id="be891-159">O usuário deve ser habilitado pela política para acessar o servidor de chat persistente.</span><span class="sxs-lookup"><span data-stu-id="be891-159">User has to be enabled by policy to access Persistent Chat Server.</span></span> <span data-ttu-id="be891-160">Por padrão, a política está desativada para todos os usuários e pode ser definida nos escopos global/site/pool/usuário.</span><span class="sxs-lookup"><span data-stu-id="be891-160">By default, the policy is turned off for all users and can be defined at global/site/pool/user scopes.</span></span></p></li>
<li><p><span data-ttu-id="be891-161">Definir configurações</span><span class="sxs-lookup"><span data-stu-id="be891-161">Configure settings</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="be891-p104">O usuário deve ser membro do CsPersistentChatAdministrator. Para alterar a política, o usuário deve estar no CsUserAdministrator, no mínimo.</span><span class="sxs-lookup"><span data-stu-id="be891-p104">User must be a member of CsPersistentChatAdministrator. To change policy, user must be in CsUserAdministrator, at a minimum.</span></span></p></td>
<td><p><span data-ttu-id="be891-164"><a href="lync-server-2013-configuring-persistent-chat-server.md">Configurando o servidor de chat persistente no Lync Server 2013</a> na documentação de implantação</span><span class="sxs-lookup"><span data-stu-id="be891-164"><a href="lync-server-2013-configuring-persistent-chat-server.md">Configuring Persistent Chat Server in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="be891-165">Você pode implantar um ou mais pools de servidores de chat persistentes.</span><span class="sxs-lookup"><span data-stu-id="be891-165">You can deploy one or more Persistent Chat Server pools.</span></span> <span data-ttu-id="be891-166">Oferecemos suporte a vários pools de servidores de chat persistentes por motivos regulatórios nos quais os dados gerados em determinada região são necessários para permanecer nessa região.</span><span class="sxs-lookup"><span data-stu-id="be891-166">We support multiple Persistent Chat Server pools for regulatory reasons whereby data generated in a given region is required to stay in that region.</span></span> <span data-ttu-id="be891-167">Por exemplo, se você implantar um pool de servidores de chat persistente em Chicago e outro em Zurique para ficar em conformidade com as normas de dados na Suíça, os usuários poderão se conectar a salas nos pools de servidores de chat persistentes, contanto que tenham acesso.</span><span class="sxs-lookup"><span data-stu-id="be891-167">For example, if you deploy a Persistent Chat Server pool in Chicago, and another in Zurich to comply with regulations for data in Switzerland, users can connect to rooms in both the Persistent Chat Server pools, provided they have access.</span></span>



<span data-ttu-id="be891-168"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be891-168"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

