---
title: 'Lync Server 2013: Permissões e pré-requisitos de configuração de Grupo de Resposta'
description: 'Lync Server 2013: permissões e pré-requisitos de configuração do grupo de respostas.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response Group configuration permissions and prerequisites
ms:assetid: 4266f16a-b387-452c-a8ca-d771a3c58f0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204840(v=OCS.15)
ms:contentKeyID: 48183972
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7a0548c1d8886eb7741d1a31b24b480c1a2d30f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436311"
---
# <a name="response-group-configuration-permissions-and-prerequisites-in-lync-server-2013"></a><span data-ttu-id="57707-103">Permissões e pré-requisitos de configuração de Grupo de Resposta no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57707-103">Response Group configuration permissions and prerequisites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="57707-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="57707-104">

<span> </span></span></span>

<span data-ttu-id="57707-105">_**Tópico da última modificação:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="57707-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="57707-106">O grupo de resposta é um recurso de gerenciamento de chamadas de voz corporativa.</span><span class="sxs-lookup"><span data-stu-id="57707-106">Response Group is an Enterprise Voice call management feature.</span></span> <span data-ttu-id="57707-107">Este tópico descreve o que você precisa ter em vigor antes de poder configurar o grupo de resposta e as permissões e credenciais administrativas necessárias para executar tarefas de configuração.</span><span class="sxs-lookup"><span data-stu-id="57707-107">This topic describes what you need to have in place before you can configure Response Group and the administrative credentials and permissions you need to perform configuration tasks.</span></span>

<span data-ttu-id="57707-108">Esta seção pressupõe que você leu a documentação de planejamento relacionada ao grupo de resposta.</span><span class="sxs-lookup"><span data-stu-id="57707-108">This section assumes that you have read the planning documentation related to Response Group.</span></span> <span data-ttu-id="57707-109">Para obter detalhes, consulte [planejando os recursos de gerenciamento de chamadas no Lync Server 2013](lync-server-2013-planning-for-call-management-features.md) na documentação de planejamento.</span><span class="sxs-lookup"><span data-stu-id="57707-109">For details, see [Planning for call management features in Lync Server 2013](lync-server-2013-planning-for-call-management-features.md) in the Planning documentation.</span></span>

<div>

## <a name="configuration-tools-and-administrative-roles"></a><span data-ttu-id="57707-110">Ferramentas de configuração e funções administrativas</span><span class="sxs-lookup"><span data-stu-id="57707-110">Configuration Tools and Administrative Roles</span></span>

<span data-ttu-id="57707-111">Você pode usar as seguintes ferramentas administrativas para configurar o grupo de resposta:</span><span class="sxs-lookup"><span data-stu-id="57707-111">You can use the following administrative tools to configure Response Group:</span></span>

  - <span data-ttu-id="57707-112">Painel de Controle do Lync Server</span><span class="sxs-lookup"><span data-stu-id="57707-112">Lync Server Control Panel</span></span>

  - <span data-ttu-id="57707-113">Ferramenta de Configuração de Grupo de Resposta</span><span class="sxs-lookup"><span data-stu-id="57707-113">Response Group Configuration Tool</span></span>

  - <span data-ttu-id="57707-114">Shell de Gerenciamento do Lync Server</span><span class="sxs-lookup"><span data-stu-id="57707-114">Lync Server Management Shell</span></span>

<span data-ttu-id="57707-115">Para configurar grupos de resposta, você deve ser membro de pelo menos uma das funções administrativas a seguir:</span><span class="sxs-lookup"><span data-stu-id="57707-115">To configure response groups, you must be a member of at least one of the following administrative roles:</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57707-116"><strong>Grupo de segurança do Diretório Ativo(1)</strong></span><span class="sxs-lookup"><span data-stu-id="57707-116"><strong>Active Directory Security Group (1)</strong></span></span></p></td>
<td><p><span data-ttu-id="57707-117">Criar fluxo de trabalho</span><span class="sxs-lookup"><span data-stu-id="57707-117">Create Workflow</span></span></p></td>
<td><p><span data-ttu-id="57707-118">Atribuir gerente</span><span class="sxs-lookup"><span data-stu-id="57707-118">Assign Manager</span></span></p></td>
<td><p><span data-ttu-id="57707-119">Criar/atribuir agentes, filas</span><span class="sxs-lookup"><span data-stu-id="57707-119">Create /assign agents, queues</span></span></p></td>
<td><p><span data-ttu-id="57707-120">Criar/gerenciar horas extras e de feriado</span><span class="sxs-lookup"><span data-stu-id="57707-120">Create / manage holiday and business hours</span></span></p></td>
<td><p><span data-ttu-id="57707-121">Ativar/Desativar fluxo de trabalho</span><span class="sxs-lookup"><span data-stu-id="57707-121">Activate / deactivate workflow</span></span></p></td>
<td><p><span data-ttu-id="57707-122">Configurar fluxo de trabalho (IVR ou Grupo de busca)</span><span class="sxs-lookup"><span data-stu-id="57707-122">Configure workflow (IVR or Hunt Group)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57707-123"><strong>CsResponseGroupAdministrator</strong></span><span class="sxs-lookup"><span data-stu-id="57707-123"><strong>CsResponseGroupAdministrator</strong></span></span></p></td>
<td><p><span data-ttu-id="57707-124">√</span><span class="sxs-lookup"><span data-stu-id="57707-124">√</span></span></p></td>
<td><p><span data-ttu-id="57707-125">√</span><span class="sxs-lookup"><span data-stu-id="57707-125">√</span></span></p></td>
<td><p><span data-ttu-id="57707-126">√</span><span class="sxs-lookup"><span data-stu-id="57707-126">√</span></span></p></td>
<td><p><span data-ttu-id="57707-127">√</span><span class="sxs-lookup"><span data-stu-id="57707-127">√</span></span></p></td>
<td><p><span data-ttu-id="57707-128">√</span><span class="sxs-lookup"><span data-stu-id="57707-128">√</span></span></p></td>
<td><p><span data-ttu-id="57707-129">√</span><span class="sxs-lookup"><span data-stu-id="57707-129">√</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57707-130"><strong>CsResponseGroupManager</strong></span><span class="sxs-lookup"><span data-stu-id="57707-130"><strong>CsResponseGroupManager</strong></span></span></p></td>
<td> </td>
<td><p><span data-ttu-id="57707-131">√(2)</span><span class="sxs-lookup"><span data-stu-id="57707-131">√(2)</span></span></p></td>
<td><p><span data-ttu-id="57707-132">√(3)</span><span class="sxs-lookup"><span data-stu-id="57707-132">√(3)</span></span></p></td>
<td><p><span data-ttu-id="57707-133">√(3)</span><span class="sxs-lookup"><span data-stu-id="57707-133">√(3)</span></span></p></td>
<td><p><span data-ttu-id="57707-134">√(3)</span><span class="sxs-lookup"><span data-stu-id="57707-134">√(3)</span></span></p></td>
<td><p><span data-ttu-id="57707-135">√(3)</span><span class="sxs-lookup"><span data-stu-id="57707-135">√(3)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57707-136"><strong>CsVoiceAdministrator</strong></span><span class="sxs-lookup"><span data-stu-id="57707-136"><strong>CsVoiceAdministrator</strong></span></span></p></td>
<td><p><span data-ttu-id="57707-137">√</span><span class="sxs-lookup"><span data-stu-id="57707-137">√</span></span></p></td>
<td><p><span data-ttu-id="57707-138">√</span><span class="sxs-lookup"><span data-stu-id="57707-138">√</span></span></p></td>
<td><p><span data-ttu-id="57707-139">√</span><span class="sxs-lookup"><span data-stu-id="57707-139">√</span></span></p></td>
<td><p><span data-ttu-id="57707-140">√</span><span class="sxs-lookup"><span data-stu-id="57707-140">√</span></span></p></td>
<td><p><span data-ttu-id="57707-141">√</span><span class="sxs-lookup"><span data-stu-id="57707-141">√</span></span></p></td>
<td><p><span data-ttu-id="57707-142">√</span><span class="sxs-lookup"><span data-stu-id="57707-142">√</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57707-143"><strong>CsServerAdministrator</strong></span><span class="sxs-lookup"><span data-stu-id="57707-143"><strong>CsServerAdministrator</strong></span></span></p></td>
<td><p><span data-ttu-id="57707-144">√</span><span class="sxs-lookup"><span data-stu-id="57707-144">√</span></span></p></td>
<td><p><span data-ttu-id="57707-145">√</span><span class="sxs-lookup"><span data-stu-id="57707-145">√</span></span></p></td>
<td><p><span data-ttu-id="57707-146">√</span><span class="sxs-lookup"><span data-stu-id="57707-146">√</span></span></p></td>
<td><p><span data-ttu-id="57707-147">√</span><span class="sxs-lookup"><span data-stu-id="57707-147">√</span></span></p></td>
<td><p><span data-ttu-id="57707-148">√</span><span class="sxs-lookup"><span data-stu-id="57707-148">√</span></span></p></td>
<td><p><span data-ttu-id="57707-149">√</span><span class="sxs-lookup"><span data-stu-id="57707-149">√</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57707-150"><strong>CsAdministrator</strong></span><span class="sxs-lookup"><span data-stu-id="57707-150"><strong>CsAdministrator</strong></span></span></p></td>
<td><p><span data-ttu-id="57707-151">√</span><span class="sxs-lookup"><span data-stu-id="57707-151">√</span></span></p></td>
<td><p><span data-ttu-id="57707-152">√</span><span class="sxs-lookup"><span data-stu-id="57707-152">√</span></span></p></td>
<td><p><span data-ttu-id="57707-153">√</span><span class="sxs-lookup"><span data-stu-id="57707-153">√</span></span></p></td>
<td><p><span data-ttu-id="57707-154">√</span><span class="sxs-lookup"><span data-stu-id="57707-154">√</span></span></p></td>
<td><p><span data-ttu-id="57707-155">√</span><span class="sxs-lookup"><span data-stu-id="57707-155">√</span></span></p></td>
<td><p><span data-ttu-id="57707-156">√</span><span class="sxs-lookup"><span data-stu-id="57707-156">√</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57707-157"><strong>CsViewOnlyAdministrator</strong></span><span class="sxs-lookup"><span data-stu-id="57707-157"><strong>CsViewOnlyAdministrator</strong></span></span></p></td>
<td><p><span data-ttu-id="57707-158">√(4)</span><span class="sxs-lookup"><span data-stu-id="57707-158">√(4)</span></span></p></td>
<td><p><span data-ttu-id="57707-159">√(4)</span><span class="sxs-lookup"><span data-stu-id="57707-159">√(4)</span></span></p></td>
<td><p><span data-ttu-id="57707-160">√(4)</span><span class="sxs-lookup"><span data-stu-id="57707-160">√(4)</span></span></p></td>
<td><p><span data-ttu-id="57707-161">√(4)</span><span class="sxs-lookup"><span data-stu-id="57707-161">√(4)</span></span></p></td>
<td><p><span data-ttu-id="57707-162">√(4)</span><span class="sxs-lookup"><span data-stu-id="57707-162">√(4)</span></span></p></td>
<td><p><span data-ttu-id="57707-163">√(4)</span><span class="sxs-lookup"><span data-stu-id="57707-163">√(4)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="57707-164"><STRONG>(1)</STRONG> um objeto de usuário dos serviços de domínio Active Directory deve ser um membro do grupo de segurança especificado do Active Directory listado.</span><span class="sxs-lookup"><span data-stu-id="57707-164"><STRONG>(1)</STRONG> An Active Directory Domain Services user object must be a member of the specified Active Directory security group listed.</span></span> <span data-ttu-id="57707-165">Um administrador ou outro membro de grupo delegado do Active Directory com permissões adequadas para adicionar usuários a um grupo de segurança (por exemplo, administrador, operadores de conta) devem adicionar um objeto de usuário ao grupo ou grupo de segurança listado para que o usuário possa executar as funções listadas.</span><span class="sxs-lookup"><span data-stu-id="57707-165">An administrator or other delegated Active Directory group member with appropriate permissions to add users to a security group (For example, Administrator, Account Operators) must add a user object to the listed security group or group for the user to be able to perform the functions listed.</span></span> <span data-ttu-id="57707-166"><STRONG>(2)</STRONG> somente para fluxos de trabalho que o CsResponseGroupAdministrator atribuiu ao CsResponseGroupManager.</span><span class="sxs-lookup"><span data-stu-id="57707-166"><STRONG>(2)</STRONG> Only for workflows that the CsResponseGroupAdministrator has assigned to the CsResponseGroupManager.</span></span> <span data-ttu-id="57707-167"><STRONG>(3)</STRONG> um gerente de grupo de resposta pode atribuir outro membro de CsResponseGroupManager a um fluxo de trabalho que o gerente atual já gerencia.</span><span class="sxs-lookup"><span data-stu-id="57707-167"><STRONG>(3)</STRONG> A Response Group Manager can assign another member of CsResponseGroupManager to a workflow that the current manager already manages.</span></span> <span data-ttu-id="57707-168"><STRONG>(4)</STRONG> CsViewOnlyAdministrator só pode executar cmdlets do Shell de gerenciamento do Lync Server "Get" do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="57707-168"><STRONG>(4)</STRONG> CsViewOnlyAdministrator can only run verb "Get" Lync Server Management Shell cmdlets.</span></span>



</div>

</div>

<div>

## <a name="response-group-configuration-prerequisites"></a><span data-ttu-id="57707-169">Requisitos de configuração do grupo de resposta</span><span class="sxs-lookup"><span data-stu-id="57707-169">Response Group Configuration Prerequisites</span></span>

<span data-ttu-id="57707-170">O grupo de resposta requer os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="57707-170">Response Group requires the following components:</span></span>

  - <span data-ttu-id="57707-171">Serviço de aplicativos</span><span class="sxs-lookup"><span data-stu-id="57707-171">Application service</span></span>

  - <span data-ttu-id="57707-172">Aplicativo Grupo de Resposta</span><span class="sxs-lookup"><span data-stu-id="57707-172">Response Group application</span></span>

  - <span data-ttu-id="57707-173">Pacotes de idioma</span><span class="sxs-lookup"><span data-stu-id="57707-173">Language packs</span></span>

  - <span data-ttu-id="57707-174">Repositório de arquivos (para manter arquivos de áudio)</span><span class="sxs-lookup"><span data-stu-id="57707-174">File store (to hold audio files)</span></span>

  - <span data-ttu-id="57707-175">Serviços Web (inclui a ferramenta de configuração de grupo de resposta e o console de entrada e saída dos agentes)</span><span class="sxs-lookup"><span data-stu-id="57707-175">Web Services (includes the Response Group Configuration Tool and the agents' sign-in and sign-out console)</span></span>

<span data-ttu-id="57707-176">Todos esses componentes são instalados por padrão quando você implanta o Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="57707-176">All of these components are installed by default when you deploy Enterprise Voice.</span></span>

<span data-ttu-id="57707-177">Talvez seja necessário executar as seguintes tarefas antes de configurar o grupo de resposta:</span><span class="sxs-lookup"><span data-stu-id="57707-177">You might need to perform the following tasks before configuring Response Group:</span></span>

  - <span data-ttu-id="57707-178">Habilite os usuários do Lync Server 2013 e do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="57707-178">Enable users for Lync Server 2013 and Enterprise Voice.</span></span>

  - <span data-ttu-id="57707-179">Modificar um arquivo de configuração para estar em conformidade com os Padrões de Processamento de Informação Federal (FIPS).</span><span class="sxs-lookup"><span data-stu-id="57707-179">Modify a configuration file to be compliant with Federal Information Processing Standards (FIPS).</span></span>

  - <span data-ttu-id="57707-180">Modificar o agrupamento do banco de dados para suportar caracteres Yi, Meng, e Zang para nomes de fila e nomes de grupo de agentes.</span><span class="sxs-lookup"><span data-stu-id="57707-180">Modify the database collation to support Yi, Meng, and Zang characters for queue names and agent group names.</span></span>

<div>

## <a name="enabling-users"></a><span data-ttu-id="57707-181">Ativando usuários</span><span class="sxs-lookup"><span data-stu-id="57707-181">Enabling Users</span></span>

<span data-ttu-id="57707-182">A primeira etapa na configuração do grupo de resposta é criar grupos de agente.</span><span class="sxs-lookup"><span data-stu-id="57707-182">The first step in configuring Response Group is to create agent groups.</span></span> <span data-ttu-id="57707-183">Antes de poder criar um grupo de agente, você deve habilitar os usuários que serão agentes para o grupo de resposta do Lync Server 2013 e Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="57707-183">Before you can create an agent group, you must enable the users who will be agents for Response Group for Lync Server 2013 and Enterprise Voice.</span></span> <span data-ttu-id="57707-184">Habilitar usuários para o Lync Server 2013 normalmente é uma etapa na implantação do servidor Enterprise Edition Server ou Standard Edition Server.</span><span class="sxs-lookup"><span data-stu-id="57707-184">Enabling users for Lync Server 2013 is typically a step in the Enterprise Edition server or Standard Edition server deployment.</span></span> <span data-ttu-id="57707-185">Para obter detalhes sobre como habilitar usuários do Lync Server 2013, consulte [desabilitar ou habilitar novamente a conta de usuário para o Lync server 2013](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md).</span><span class="sxs-lookup"><span data-stu-id="57707-185">For details about enabling users for Lync Server 2013, see [Disable or re-enable user account for Lync Server 2013](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md).</span></span> <span data-ttu-id="57707-186">A habilitação dos usuários para o Enterprise Voice geralmente é uma etapa na implantação do Enterprise Voice.</span><span class="sxs-lookup"><span data-stu-id="57707-186">Enabling users for Enterprise Voice is typically a step in the Enterprise Voice deployment.</span></span> <span data-ttu-id="57707-187">Para obter detalhes, consulte [habilitar usuários do Enterprise Voice no Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span><span class="sxs-lookup"><span data-stu-id="57707-187">For details, see [Enable users for Enterprise Voice in Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span></span>

</div>

<div>

## <a name="complying-with-fips-requirements"></a><span data-ttu-id="57707-188">Em conformidade com os requisitos FIPS</span><span class="sxs-lookup"><span data-stu-id="57707-188">Complying with FIPS requirements</span></span>

<span data-ttu-id="57707-189">Essa seção se aplica a você apenas se sua organização precisar estar em conformidade com os Padrões de Processamento de Informações Federais (FIPS).</span><span class="sxs-lookup"><span data-stu-id="57707-189">This section applies to you only if your organization needs to comply with Federal Information Processing Standards (FIPS).</span></span>

<span data-ttu-id="57707-190">Para estar em conformidade com FIPS, você precisa modificar o nível de aplicativo do arquivo Web.config para utilizar um algoritmo de criptografia diferente após instalar os Serviços Web.</span><span class="sxs-lookup"><span data-stu-id="57707-190">To be compliant with FIPS, you need to modify the application-level Web.config file to use a different cryptography algorithm after you install Web Services.</span></span> <span data-ttu-id="57707-191">Você precisa especificar que o ASP.NET utiliza o algoritmo do Padrão de Criptografia de Dados Triplo (3DES) para processar dados de estado de visualização.</span><span class="sxs-lookup"><span data-stu-id="57707-191">You need to specify that ASP.NET use the Triple Data Encryption Standard (3DES) algorithm to process view state data.</span></span> <span data-ttu-id="57707-192">Para o aplicativo de grupo de resposta, esse requisito se aplica à ferramenta de configuração de grupo de resposta e ao console de entrada e saída do agente.</span><span class="sxs-lookup"><span data-stu-id="57707-192">For the Response Group application, this requirement applies to the Response Group Configuration Tool and the agent sign-in and sign-out console.</span></span> <span data-ttu-id="57707-193">Para obter detalhes sobre esse requisito, consulte o artigo 911722 da base de dados de conhecimento Microsoft, "você pode receber uma mensagem de erro ao acessar páginas da Web do ASP.NET com ViewState habilitado após a atualização do ASP.NET 1,1 para o ASP.NET 2,0," at [https://go.microsoft.com/fwlink/p/?linkId=196183](https://go.microsoft.com/fwlink/p/?linkid=196183) .</span><span class="sxs-lookup"><span data-stu-id="57707-193">For details about this requirement, see Microsoft Knowledge Base article 911722, "You may receive an error message when you access ASP.NET webpages that have ViewState enabled after you upgrade from ASP.NET 1.1 to ASP.NET 2.0," at [https://go.microsoft.com/fwlink/p/?linkId=196183](https://go.microsoft.com/fwlink/p/?linkid=196183).</span></span>

<span data-ttu-id="57707-194">Para modificar o arquivo Web.config, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="57707-194">To modify the Web.config file, do the following:</span></span>

1.  <span data-ttu-id="57707-195">Em um editor de texto como o Notepad, abra o arquivo Web.config de nível de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="57707-195">In a text editor such as Notepad, open the application-level Web.config file.</span></span>

2.  <span data-ttu-id="57707-196">No arquivo Web.config, localize a `<system.web>` seção.</span><span class="sxs-lookup"><span data-stu-id="57707-196">In the Web.config file, locate the `<system.web>` section.</span></span>

3.  <span data-ttu-id="57707-197">Adicione a seguinte `<machineKey>` seção à `<system.web>` seção:</span><span class="sxs-lookup"><span data-stu-id="57707-197">Add the following `<machineKey>` section to in the `<system.web>` section:</span></span>
    
        <machineKey validationKey="AutoGenerate,IsolateApps" decryptionKey="AutoGenerate,IsolateApps" validation="3DES" decryption="3DES"/>

4.  <span data-ttu-id="57707-198">Salve o arquivo Web.config.</span><span class="sxs-lookup"><span data-stu-id="57707-198">Save the Web.config file.</span></span>

5.  <span data-ttu-id="57707-199">Reinicie o serviço de serviços de informações da Internet (IIS) executando o seguinte comando em um prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="57707-199">Restart the Internet Information Services (IIS) service by running the following command at a command prompt:</span></span>
    
        iisreset

</div>

<div>

## <a name="supporting-yi-meng-and-zang-characters"></a><span data-ttu-id="57707-200">Suporte a caracteres Yi, Meng e Zang</span><span class="sxs-lookup"><span data-stu-id="57707-200">Supporting Yi, Meng, and Zang Characters</span></span>

<span data-ttu-id="57707-201">Essa seção se aplica apenas se a sua organização precisar suportar caracteres Yi, Meng ou Zang.</span><span class="sxs-lookup"><span data-stu-id="57707-201">This section applies to you only if your organization needs to support Yi, Meng, or Zang characters.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="57707-202">Para obter informações sobre o que são os caracteres Yi, Meng e Zang e por que eles podem ser importantes para a sua implantação, consulte as informações nos conjuntos de caracteres do GB18030 <A href="https://go.microsoft.com/fwlink/p/?linkid=240223">https://go.microsoft.com/fwlink/p/?linkId=240223</A> .</span><span class="sxs-lookup"><span data-stu-id="57707-202">For information on what the Yi, Meng, and Zang characters are and why they may be important to your deployment, see the information on the GB18030 character sets <A href="https://go.microsoft.com/fwlink/p/?linkid=240223">https://go.microsoft.com/fwlink/p/?linkId=240223</A>.</span></span>



</div>

<span data-ttu-id="57707-p106">Para suportar caracteres Yi, Meng ou Zang, você precisa modificar o agrupamento para o banco de dados Rgsconfig. Altere o agrupamento da coluna  **Nome** nas seguintes tabelas em cada banco de dados Rgsconfig:</span><span class="sxs-lookup"><span data-stu-id="57707-p106">To support Yi, Meng, or Zang characters, you need to modify the collation for the Rgsconfig database. Change the collation of the **Name** column in the following tables in each Rgsconfig database:</span></span>

  - <span data-ttu-id="57707-205">dbo.AgentGroups</span><span class="sxs-lookup"><span data-stu-id="57707-205">dbo.AgentGroups</span></span>

  - <span data-ttu-id="57707-206">dbo.BusinessHours</span><span class="sxs-lookup"><span data-stu-id="57707-206">dbo.BusinessHours</span></span>

  - <span data-ttu-id="57707-207">dbo.HolidaySets</span><span class="sxs-lookup"><span data-stu-id="57707-207">dbo.HolidaySets</span></span>

  - <span data-ttu-id="57707-208">dbo.Queues</span><span class="sxs-lookup"><span data-stu-id="57707-208">dbo.Queues</span></span>

  - <span data-ttu-id="57707-209">dbo.Workflows</span><span class="sxs-lookup"><span data-stu-id="57707-209">dbo.Workflows</span></span>

<span data-ttu-id="57707-210">Para SQL Server 2008 R2 e SQL Server 2012, use o \_ agrupamento latim geral \_ 100 (diferenciação de ênfase).</span><span class="sxs-lookup"><span data-stu-id="57707-210">For SQL Server 2008 R2 and SQL Server 2012, use the Latin\_General\_100 (Accent Sensitive) collation.</span></span> <span data-ttu-id="57707-211">Se você utiliza tal agrupamento, todos os nomes de objeto não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="57707-211">If you use this collation, all object names are not case-sensitive.</span></span>

<span data-ttu-id="57707-212">Você pode mudar o agrupamento utilizando o Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="57707-212">You can change the collation by using Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="57707-213">Para obter detalhes sobre como usar essa ferramenta, consulte "usando o SQL Server Management Studio" em [https://go.microsoft.com/fwlink/p/?linkId=196184](https://go.microsoft.com/fwlink/p/?linkid=196184) .</span><span class="sxs-lookup"><span data-stu-id="57707-213">For details about using this tool, see "Using SQL Server Management Studio" at [https://go.microsoft.com/fwlink/p/?linkId=196184](https://go.microsoft.com/fwlink/p/?linkid=196184).</span></span> <span data-ttu-id="57707-214">Siga essas etapas para alterar o agrupamento:</span><span class="sxs-lookup"><span data-stu-id="57707-214">Follow these steps to change the collation:</span></span>

1.  <span data-ttu-id="57707-215">Certifique-se de que o SQL Server Management Studio está configurado para permitir alterações que precisam que as tabelas sejam recriadas.</span><span class="sxs-lookup"><span data-stu-id="57707-215">Be sure that SQL Server Management Studio is configured to allow changes that require tables to be recreated.</span></span> <span data-ttu-id="57707-216">Para obter detalhes, consulte a caixa de diálogo "salvar (não permitido)" em [https://go.microsoft.com/fwlink/p/?linkId=196186](https://go.microsoft.com/fwlink/p/?linkid=196186) .</span><span class="sxs-lookup"><span data-stu-id="57707-216">For details, see "Save (Not Permitted) Dialog Box" at [https://go.microsoft.com/fwlink/p/?linkId=196186](https://go.microsoft.com/fwlink/p/?linkid=196186).</span></span> <span data-ttu-id="57707-217">Para obter detalhes sobre como definir um agrupamento de colunas, consulte "como: definir o agrupamento de colunas (ferramentas de banco de dados Visual)" em [https://go.microsoft.com/fwlink/p/?linkId=196185](https://go.microsoft.com/fwlink/p/?linkid=196185) .</span><span class="sxs-lookup"><span data-stu-id="57707-217">For details about setting a column collation, see "How to: Set Column Collation (Visual Database Tools)" at [https://go.microsoft.com/fwlink/p/?linkId=196185](https://go.microsoft.com/fwlink/p/?linkid=196185).</span></span>

2.  <span data-ttu-id="57707-218">Utilizando o Microsoft SQL Server Management Studio, conecte-se ao banco de dados Rgsconfig.</span><span class="sxs-lookup"><span data-stu-id="57707-218">Using Microsoft SQL Server Management Studio, connect to the Rgsconfig database.</span></span>

3.  <span data-ttu-id="57707-219">Encontre a tabela que deseja alterar no banco de dados Rgsconfig, clique com o botão direito na tabela e em **Design**.</span><span class="sxs-lookup"><span data-stu-id="57707-219">Find the table you want to change in the Rgsconfig database, right-click the table, and click **Design**.</span></span>

4.  <span data-ttu-id="57707-220">Altere o agrupamento da coluna **Nome** e salve a tabela.</span><span class="sxs-lookup"><span data-stu-id="57707-220">Change the collation of the **Name** column and save the table.</span></span>

<span data-ttu-id="57707-221"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="57707-221"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

