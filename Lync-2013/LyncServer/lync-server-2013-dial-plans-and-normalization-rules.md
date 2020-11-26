---
title: 'Lync Server 2013: planos de discagem e regras de normalização'
description: 'Lync Server 2013: planos de discagem e regras de normalização.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dial plans and normalization rules
ms:assetid: fde45195-6eb4-403c-9094-57df7fc0bd2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413082(v=OCS.15)
ms:contentKeyID: 48185960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0341d0c5267a2272ff45bd93408b2bd14f0ceeaa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429207"
---
# <a name="dial-plans-and-normalization-rules-in-lync-server-2013"></a><span data-ttu-id="0a8f2-103">Planos de discagem e regras de normalização no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0a8f2-103">Dial plans and normalization rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0a8f2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0a8f2-104">

<span> </span></span></span>

<span data-ttu-id="0a8f2-105">_**Tópico da última modificação:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="0a8f2-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="0a8f2-106">Um plano de discagem é um conjunto nomeado de regras de normalização que converte números de telefone de um local nomeado, usuário individual ou objeto de contato em um único formato padrão (E.164) para fins de roteamento de chamadas e autorização de telefones.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-106">A dial plan is a named set of normalization rules that translates phone numbers for a named location, individual user, or contact object into a single standard (E.164) format for purposes of phone authorization and call routing.</span></span>

<span data-ttu-id="0a8f2-p101">As regras de normalização definem como os números de telefone expressos em vários formatos devem ser roteados para cada local, usuário ou objeto de contato especificado. A mesma sequência de discagem pode ser interpretada e convertida de forma diferente dependendo do local do qual ele é discado e da pessoa ou do objeto de contato que está fazendo a chamada.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-p101">Normalization rules define how phone numbers expressed in various formats are to be routed for each specified location, user, or contact object. The same dial string may be interpreted and translated differently, depending on the location from which it is dialed and the person or contact object making the call.</span></span>

<div>

## <a name="dial-plan-scope"></a><span data-ttu-id="0a8f2-109">Escopo do plano de discagem</span><span class="sxs-lookup"><span data-stu-id="0a8f2-109">Dial Plan Scope</span></span>

<span data-ttu-id="0a8f2-110">Um *escopo* do plano de discagem determina o nível hierárquico em que o plano de discagem pode ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-110">A dial plan’s *scope* determines the hierarchical level at which the dial plan can be applied.</span></span> <span data-ttu-id="0a8f2-111">No Lync Server, um usuário pode receber um plano de discagem específico por usuário.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-111">In Lync Server, a user can be assigned a specific per-user dial plan.</span></span> <span data-ttu-id="0a8f2-112">Se um plano de discagem do usuário não for atribuído, o plano de discagem do pool do registrador será aplicado.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-112">If a user dial plan is not assigned, the Registrar pool dial plan is applied.</span></span> <span data-ttu-id="0a8f2-113">Se não houver um plano de discagem do pool de registrador, o plano de discagem de site será aplicado.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-113">If there is no Registrar pool dial plan, the site dial plan is applied.</span></span> <span data-ttu-id="0a8f2-114">Finalmente, se não houver nenhum outro plano de discagem aplicável ao usuário, o plano de discagem global será aplicado.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-114">Finally, if there is no other dial plan applicable to the user, the global dial plan is applied.</span></span>

<span data-ttu-id="0a8f2-115">Os clientes obtêm níveis de escopo de plano de discagem por meio das configurações de provisionamento em banda fornecidas quando os usuários fazem logon no Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-115">Clients obtain dial plan scope levels through in-band provisioning settings that are provided when users log on to Lync Server.</span></span> <span data-ttu-id="0a8f2-116">Como administrador, você pode gerenciar e atribuir níveis de escopo do plano de discagem usando o painel de controle do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-116">As the administrator, you can manage and assign dial plan scope levels by using Lync Server Control Panel.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0a8f2-117">O plano de discagem de gateway PSTN (Rede Telefônica Pública Comutada) em nível de serviço é aplicado às chamadas de entrada de um gateway específico.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-117">The service level public switched telephone network (PSTN) gateway dial plan is applied to the incoming calls from a particular gateway.</span></span>



</div>

<span data-ttu-id="0a8f2-118">Os níveis de escopo do plano de discagem são definidos como a seguir:</span><span class="sxs-lookup"><span data-stu-id="0a8f2-118">Dial plan scope levels are defined as follows:</span></span>

  - <span data-ttu-id="0a8f2-119">**Plano de discagem do usuário:** Pode ser atribuído a usuários, grupos ou objetos de contato individuais.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-119">**User dial plan:** Can be assigned to individual users, groups, or contact objects.</span></span> <span data-ttu-id="0a8f2-120">Os aplicativos de voz podem pesquisar um plano de discagem por usuário quando uma chamada é recebida com o contexto de telefone definido para padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-120">Voice applications can look up a per-user dial plan when a call is received with the phone-context set to user-default.</span></span> <span data-ttu-id="0a8f2-121">Para atribuir um plano de discagem, um objeto de contato é tratado como um usuário individual.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-121">For the purpose of assigning a dial plan, a contact object is treated as an individual user.</span></span>

  - <span data-ttu-id="0a8f2-122">**Plano de discagem de pool:** Pode ser criado no nível de serviço para qualquer serviço de gateway ou registrador PSTN em sua topologia.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-122">**Pool dial plan:** Can be created at the service level for any PSTN gateway or Registrar in your topology.</span></span> <span data-ttu-id="0a8f2-123">Para definir um plano de discagem do pool, você deve especificar o serviço (gateway PSTN ou pool do Registrador Avançado) ao qual o plano de discagem se aplica.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-123">To define a pool dial plan, you must specify the particular service (PSTN gateway or Registrar pool) to which the dial plan applies.</span></span>

  - <span data-ttu-id="0a8f2-124">**Plano de discagem de site:** Pode ser criado para um site inteiro, exceto para qualquer usuário, grupo ou objeto de contato que receba um plano de discagem de pool ou um plano de discagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-124">**Site dial plan:** Can be created for an entire site, except for any users, groups, or contact objects that are assigned a pool dial plan or user dial plan.</span></span> <span data-ttu-id="0a8f2-125">Para definir um plano de discagem do local, você deve especificar o local ao qual o plano de discagem é aplicado.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-125">To define a site dial plan, you must specify the site to which the dial plan applies.</span></span>

  - <span data-ttu-id="0a8f2-126">**Plano de discagem global:** O plano de discagem padrão instalado com o produto.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-126">**Global dial plan:** The default dial plan installed with the product.</span></span> <span data-ttu-id="0a8f2-127">É possível editar o plano de discagem global, mas não excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-127">You can edit the global dial plan, but you cannot delete it.</span></span> <span data-ttu-id="0a8f2-128">Este plano de discagem aplica-se a todos os usuários do Enterprise Voice, grupos e objetos de contato na sua implantação, a menos que você configure e atribua um plano de discagem com um escopo mais específico.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-128">This dial plan applies to all Enterprise Voice users, groups, and contact objects in your deployment, unless you configure and assign a dial plan with a more specific scope.</span></span>

</div>

<div>

## <a name="planning-for-dial-plans"></a><span data-ttu-id="0a8f2-129">Planejamento de planos de discagem</span><span class="sxs-lookup"><span data-stu-id="0a8f2-129">Planning for Dial Plans</span></span>

<span data-ttu-id="0a8f2-130">Para planejar uma discagem, siga estas instruções:</span><span class="sxs-lookup"><span data-stu-id="0a8f2-130">To plan a dial plan, follow these steps:</span></span>

  - <span data-ttu-id="0a8f2-131">Liste todas as localidades nas quais a organização tem escritórios.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-131">List all the locales in which your organization has an office.</span></span>
    
    <span data-ttu-id="0a8f2-p108">A lista deve estar atualizada e ser completa. Precisará ser revisada conforme a organização da empresa evolui. Em uma grande empresa multinacional com várias filiais pequenas, isso pode ser uma tarefa demorada.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-p108">The list must be up-to-date and complete. It will need to be revised as company organization evolves. In a large, multinational company with numerous small branch offices, this can be a time-consuming task.</span></span>

  - <span data-ttu-id="0a8f2-135">Identifique padrões de números válidos para cada local.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-135">Identify valid number patterns for each site.</span></span>
    
    <span data-ttu-id="0a8f2-p109">A parte mais demorada do planejamento de seus planos de discagem é identificar os padrões de números válidos para cada local. Em alguns casos, será possível copiar as regras de normalização gravadas para um plano de discagem a outros planos de discagem, especialmente se os locais correspondentes estão dentro do mesmo país/região ou continente. Em outros casos, as pequenas alterações em números em um plano de discagem podem ser suficientes para usá-los em outros planos de discagem.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-p109">The most time-consuming part of planning your dial plans is identifying the valid number patterns for each site. In some cases, you may be able to copy normalization rules that you have written for one dial plan to other dial plans, especially if the corresponding sites are within the same country/region or even continent. In other cases, small changes to numbers in one dial plan may be enough to use them in other dial plans.</span></span>

  - <span data-ttu-id="0a8f2-139">Desenvolva um esquema em toda a organização para nomear os planos de discagem.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-139">Develop an organization-wide scheme for naming dial plans.</span></span>
    
    <span data-ttu-id="0a8f2-140">Adotar um esquema de nomeação padrão garante a consistência em toda a organização e facilita a manutenção e as atualizações.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-140">Adopting a standard naming scheme assures consistency across an organization and makes maintenance and updates easier.</span></span>

  - <span data-ttu-id="0a8f2-141">Decida se vários planos de discagem são necessários para um único local.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-141">Decide whether multiple dial plans are required for a single location.</span></span>
    
    <span data-ttu-id="0a8f2-142">Se a sua organização mantiver um único plano de discagem entre vários locais, talvez ainda seja necessário criar um plano de discagem separado para os usuários do Enterprise Voice que estão migrando de um PBX (Private Branch Exchange) e que precisem ter as extensões existentes retidas.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-142">If your organization maintains a single dial plan across multiple locations, you may still need to create a separate dial plan for Enterprise Voice users who are migrating from a private branch exchange (PBX) and who need to have their existing extensions retained.</span></span>

  - <span data-ttu-id="0a8f2-143">Decida se os planos de discagem por usuário são necessários.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-143">Decide whether per-user dial plans are required.</span></span> <span data-ttu-id="0a8f2-144">Por exemplo, se você tiver usuários em um site de filiais registrados no site central ou se tiver usuários registrados em um aparelho de ramificação sobreviventes, você pode considerar cenários de discagem especiais para tais usuários usando planos de discagem por usuário e regras de normalização.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-144">For example, if you have users at a branch site who are registered with the central site or if you have users who are registered on a Survivable Branch Appliance, you can consider special dialing scenarios for such users using per-user dial plans and normalization rules.</span></span> <span data-ttu-id="0a8f2-145">Para obter detalhes, consulte [requisitos de resiliência de site de filial para o Lync Server 2013](lync-server-2013-branch-site-resiliency-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f2-145">For details, see [Branch-site resiliency requirements for Lync Server 2013](lync-server-2013-branch-site-resiliency-requirements.md).</span></span>

  - <span data-ttu-id="0a8f2-146">Determine o escopo do plano de discagem (como descrito anteriormente neste tópico).</span><span class="sxs-lookup"><span data-stu-id="0a8f2-146">Determine dial plan scope (as previously described in this topic).</span></span>

<span data-ttu-id="0a8f2-147">Para criar um plano de discagem, especifique valores nos campos a seguir, conforme necessário, usando o painel de controle do Lync Server ou o Shell de gerenciamento do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-147">To create a dial plan, you specify values in the following fields, as required, by using Lync Server Control Panel or Lync Server Management Shell.</span></span>

<div>

## <a name="name-and-simple-name"></a><span data-ttu-id="0a8f2-148">Nome e nome simples</span><span class="sxs-lookup"><span data-stu-id="0a8f2-148">Name and Simple Name</span></span>

<span data-ttu-id="0a8f2-149">Para planos de discagem do usuário, você deve especificar um nome descritivo que identifique os usuários, os grupos ou os objetos de contato aos quais o plano de discagem será atribuído.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-149">For user dial plans, you should specify a descriptive name that identifies the users, groups, or contact objects to which the dial plan will be assigned.</span></span> <span data-ttu-id="0a8f2-150">Para planos de discagem de site, o campo nome é preenchido previamente com o nome do site e não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-150">For site dial plans, the Name field is prepopulated with the site name and cannot be changed.</span></span> <span data-ttu-id="0a8f2-151">Para planos de discagem de pool, o campo nome é preenchido previamente com o gateway PSTN ou o nome de domínio totalmente qualificado (FQDN) do pool de front-end e não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-151">For pool dial plans, the Name field is prepopulated with the PSTN gateway or Front End pool fully qualified domain name (FQDN) and cannot be changed.</span></span>

<span data-ttu-id="0a8f2-152">O *nome simples* do plano de discagem é preenchido com uma cadeia de caracteres derivada do nome do plano de discagem.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-152">The dial plan *Simple Name* is prepopulated with a string that is derived from the dial plan name.</span></span> <span data-ttu-id="0a8f2-153">O campo Nome Simples é editável, o que permite criar uma convenção de nomenclatura mais descritiva para os planos de discagem.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-153">The Simple Name field is editable, which enables you to create a more descriptive naming convention for your dial plans.</span></span> <span data-ttu-id="0a8f2-154">O valor de *Nome Simples* não pode estar vazio e deve ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-154">The *Simple Name* value cannot be empty and must be unique.</span></span> <span data-ttu-id="0a8f2-155">Uma prática recomendada é desenvolver uma convenção de nomenclatura para toda a empresa e usar essa convenção consistentemente em todos os locais e usuários.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-155">A best practice is to develop a naming convention for your entire organization and then use this convention consistently across all sites and users.</span></span>

</div>

<div>

## <a name="description"></a><span data-ttu-id="0a8f2-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a8f2-156">Description</span></span>

<span data-ttu-id="0a8f2-p113">Recomendamos que você digite o nome comum reconhecível da localização geográfica à qual se aplica o plano de discagem correspondente. Por exemplo, se o nome do plano de discagem for Londres.Contoso.com, a descrição recomendada será Londres.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-p113">We recommend that you type the common, recognizable name of the geographic location to which the corresponding dial plan applies. For example, if the dial plan name is London.Contoso.com, the recommended description would be London.</span></span>

</div>

<div>

## <a name="dial-in-conferencing-region"></a><span data-ttu-id="0a8f2-159">Região da conferência discada</span><span class="sxs-lookup"><span data-stu-id="0a8f2-159">Dial-in Conferencing Region</span></span>

<span data-ttu-id="0a8f2-160">Se você estiver implantando a conferência discada, precisará especificar uma região de conferência de discagem para associar os números de acesso da conferência discada com um plano de discagem.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-160">If you are deploying dial-in conferencing, you will need to specify a dial-in conferencing region to associate dial-in conferencing access numbers with a dial plan.</span></span>

</div>

<div>

## <a name="external-access-prefix"></a><span data-ttu-id="0a8f2-161">Prefixo de acesso externo</span><span class="sxs-lookup"><span data-stu-id="0a8f2-161">External Access Prefix</span></span>

<span data-ttu-id="0a8f2-162">Você pode especificar um prefixo de acesso externo de até quatro caracteres ( \# , \* e 0-9) se os usuários precisarem discar um ou mais dígitos iniciais adicionais (por exemplo, 9) para obter uma linha externa.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-162">You can specify an external access prefix of up to four characters (\#, \*, and 0-9) if users need to dial one or more additional leading digits (for example, 9) to get an external line.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0a8f2-163">Se você especificar um prefixo de acesso externo, não precisará criar uma regra de normalização adicional para acomodar o prefixo.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-163">If you specify an external access prefix, you do not need to create an additional normalization rule to accommodate the prefix.</span></span>



</div>

</div>

</div>

<div>

## <a name="normalization-rules"></a><span data-ttu-id="0a8f2-164">Regras de normalização</span><span class="sxs-lookup"><span data-stu-id="0a8f2-164">Normalization Rules</span></span>

<span data-ttu-id="0a8f2-p114">As regras de normalização definem como os números de telefone expressos em vários formatos devem ser roteados para o local nomeado. A mesma cadeia numérica pode ser interpretada e convertida de forma diferente dependendo do local no qual ela é discada. As regras de normalização são necessárias para o roteamento de chamada porque os usuários podem, e devem, usar vários formatos ao inserir números de telefone em suas listas de contatos.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-p114">Normalization rules define how phone numbers expressed in various formats are to be routed for the named location. The same number string may be interpreted and translated differently, depending on the locale from which it is dialed. Normalization rules are necessary for call routing because users can, and do, use various formats when entering phone numbers in their Contacts lists.</span></span>

<span data-ttu-id="0a8f2-168">A normalização de números de telefone fornecidos pelo usuário oferece um formato consistente que facilita as tarefas a seguir:</span><span class="sxs-lookup"><span data-stu-id="0a8f2-168">Normalizing user-supplied phone numbers provides a consistent format that facilitates the following tasks:</span></span>

  - <span data-ttu-id="0a8f2-169">Fazer corresponder um número discado com o URI do SIP do destinatário pretendido.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-169">Match a dialed number to the intended recipient’s SIP-URI.</span></span>

  - <span data-ttu-id="0a8f2-170">Aplicar regras de autorização de discagem ao chamador.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-170">Apply dialing authorization rules to the calling party.</span></span>

<span data-ttu-id="0a8f2-171">Estes são alguns dos campos numéricos que as regras de normalização talvez precisem considerar:</span><span class="sxs-lookup"><span data-stu-id="0a8f2-171">The following number fields are among those that your normalization rules may need to account for:</span></span>

  - <span data-ttu-id="0a8f2-172">Plano de discagem</span><span class="sxs-lookup"><span data-stu-id="0a8f2-172">Dial plan</span></span>

  - <span data-ttu-id="0a8f2-173">Código do país</span><span class="sxs-lookup"><span data-stu-id="0a8f2-173">Country code</span></span>

  - <span data-ttu-id="0a8f2-174">Código de área</span><span class="sxs-lookup"><span data-stu-id="0a8f2-174">Area code</span></span>

  - <span data-ttu-id="0a8f2-175">Tamanho da extensão</span><span class="sxs-lookup"><span data-stu-id="0a8f2-175">Length of extension</span></span>

  - <span data-ttu-id="0a8f2-176">Prefixo do local</span><span class="sxs-lookup"><span data-stu-id="0a8f2-176">Site prefix</span></span>

<div>

## <a name="creating-normalization-rules"></a><span data-ttu-id="0a8f2-177">Criando regras de normalização</span><span class="sxs-lookup"><span data-stu-id="0a8f2-177">Creating Normalization Rules</span></span>

<span data-ttu-id="0a8f2-178">As regras de normalização usam expressões regulares do .NET Framework para especificar padrões de correspondência numérica que o servidor usa para converter cadeias de caracteres de discagem no formato E.164 para fins de pesquisa de número inverso.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-178">Normalization rules use .NET Framework regular expressions to specify numeric match patterns that the server uses to translate dial strings to E.164 format for the purpose of performing reverse number lookup.</span></span> <span data-ttu-id="0a8f2-179">Crie regras de normalização no painel de controle do Lync Server inserindo as expressões manualmente ou inserindo os dígitos iniciais e o comprimento das cadeias de caracteres de discagem a serem atendidas e permitindo que o painel de controle do Lync Server gere a expressão regular correspondente para você.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-179">You create normalization rules in the Lync Server Control Panel either by entering the expressions manually, or by entering the starting digits and the length of the dial strings to be matched and letting the Lync Server Control Panel generate the corresponding regular expression for you.</span></span> <span data-ttu-id="0a8f2-180">Em qualquer um desses casos, ao terminar, você poderá inserir um número de teste para verificar se a regra de normalização funciona como esperado.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-180">Either way, when you finish, you can enter a test number to verify that the normalization rule works as expected.</span></span>

<span data-ttu-id="0a8f2-181">Para obter detalhes sobre como usar expressões regulares do .NET Framework, consulte "expressões regulares do .NET Framework" em [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927) .</span><span class="sxs-lookup"><span data-stu-id="0a8f2-181">For details about using .NET Framework regular expressions, see ".NET Framework Regular Expressions" at [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927).</span></span>

</div>

<span id="BKMK_SampleNormalizationRules"></span>

<div>

## <a name="sample-normalization-rules"></a><span data-ttu-id="0a8f2-182">Exemplos de regras de normalização</span><span class="sxs-lookup"><span data-stu-id="0a8f2-182">Sample Normalization Rules</span></span>

<span data-ttu-id="0a8f2-p116">A tabela a seguir mostra exemplos de regras de normalização que são gravadas como expressões reguladores do .NET Framework. São apenas exemplos e não deve ser uma referência prescritiva para a criação de regras de normalização.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-p116">The following table shows sample normalization rules that are written as .NET Framework regular expressions. The samples are examples only and are not meant to be a prescriptive reference for creating your own normalization rules.</span></span>

### <a name="table-1normalization-rules-using-net-framework-regular-expressions"></a><span data-ttu-id="0a8f2-185">Tabela 1. Regras de normalização usando expressões regulares do .NET Framework</span><span class="sxs-lookup"><span data-stu-id="0a8f2-185">Table 1.Normalization Rules Using .NET Framework Regular Expressions</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a8f2-186">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="0a8f2-186">Rule name</span></span></th>
<th><span data-ttu-id="0a8f2-187">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a8f2-187">Description</span></span></th>
<th><span data-ttu-id="0a8f2-188">Padrão do número</span><span class="sxs-lookup"><span data-stu-id="0a8f2-188">Number pattern</span></span></th>
<th><span data-ttu-id="0a8f2-189">Conversão</span><span class="sxs-lookup"><span data-stu-id="0a8f2-189">Translation</span></span></th>
<th><span data-ttu-id="0a8f2-190">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0a8f2-190">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a8f2-191">4digitExtension</span><span class="sxs-lookup"><span data-stu-id="0a8f2-191">4digitExtension</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-192">Converte extensões de 4 dígitos</span><span class="sxs-lookup"><span data-stu-id="0a8f2-192">Translates 4-digit extensions</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-193">^ (\d {4} ) $</span><span class="sxs-lookup"><span data-stu-id="0a8f2-193">^(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-194">+1425555$1</span><span class="sxs-lookup"><span data-stu-id="0a8f2-194">+1425555$1</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-195">0100 é convertido em +14255550100</span><span class="sxs-lookup"><span data-stu-id="0a8f2-195">0100 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8f2-196">5digitExtension</span><span class="sxs-lookup"><span data-stu-id="0a8f2-196">5digitExtension</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-197">Converte extensões de 5 dígitos</span><span class="sxs-lookup"><span data-stu-id="0a8f2-197">Translates 5-digit extensions</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-198">^ 5 (\d {4} ) $</span><span class="sxs-lookup"><span data-stu-id="0a8f2-198">^5(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-199">+1425555$1</span><span class="sxs-lookup"><span data-stu-id="0a8f2-199">+1425555$1</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-200">50100 é convertido em +14255550100</span><span class="sxs-lookup"><span data-stu-id="0a8f2-200">50100 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8f2-201">7digitcallingRedmond</span><span class="sxs-lookup"><span data-stu-id="0a8f2-201">7digitcallingRedmond</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-202">Converte números de 7 dígitos em números locais de Redmond</span><span class="sxs-lookup"><span data-stu-id="0a8f2-202">Translates 7-digit numbers to Redmond local numbers</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-203">^ (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="0a8f2-203">^(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-204">+1425$1</span><span class="sxs-lookup"><span data-stu-id="0a8f2-204">+1425$1</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-205">5550100 é convertido em +14255550100</span><span class="sxs-lookup"><span data-stu-id="0a8f2-205">5550100 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8f2-206">7digitcallingDallas</span><span class="sxs-lookup"><span data-stu-id="0a8f2-206">7digitcallingDallas</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-207">Converte números de 7 dígitos em números locais de Dallas</span><span class="sxs-lookup"><span data-stu-id="0a8f2-207">Translates 7-digit numbers to Dallas local numbers</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-208">^ (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="0a8f2-208">^(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-209">+1972$1</span><span class="sxs-lookup"><span data-stu-id="0a8f2-209">+1972$1</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-210">5550100 é convertido em +19725550100</span><span class="sxs-lookup"><span data-stu-id="0a8f2-210">5550100 is translated to +19725550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8f2-211">10digitcallingUS</span><span class="sxs-lookup"><span data-stu-id="0a8f2-211">10digitcallingUS</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-212">Converte números de 10 dígitos nos Estados Unidos</span><span class="sxs-lookup"><span data-stu-id="0a8f2-212">Translates 10-digit numbers in the United States</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-213">^ (\d {10} ) $</span><span class="sxs-lookup"><span data-stu-id="0a8f2-213">^(\d{10})$</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-214">+1$1</span><span class="sxs-lookup"><span data-stu-id="0a8f2-214">+1$1</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-215">2065550100 é convertido em +12065550100</span><span class="sxs-lookup"><span data-stu-id="0a8f2-215">2065550100 is translated to +12065550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8f2-216">LDCallingUS</span><span class="sxs-lookup"><span data-stu-id="0a8f2-216">LDCallingUS</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-217">Converte números com prefixos de longa distância nos Estados Unidos</span><span class="sxs-lookup"><span data-stu-id="0a8f2-217">Translates numbers with long distance prefixes in the United States</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-218">^ 1 (\d {10} ) $</span><span class="sxs-lookup"><span data-stu-id="0a8f2-218">^1(\d{10})$</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-219">+$1</span><span class="sxs-lookup"><span data-stu-id="0a8f2-219">+$1</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-220">12145550100 é convertido em +2145550100</span><span class="sxs-lookup"><span data-stu-id="0a8f2-220">12145550100 is translated to +2145550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8f2-221">IntlCallingUS</span><span class="sxs-lookup"><span data-stu-id="0a8f2-221">IntlCallingUS</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-222">Converte números com prefixos internacionais nos Estados Unidos</span><span class="sxs-lookup"><span data-stu-id="0a8f2-222">Translates numbers with international prefixes in the United States</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-223">^011(\d\*)$</span><span class="sxs-lookup"><span data-stu-id="0a8f2-223">^011(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-224">+$1</span><span class="sxs-lookup"><span data-stu-id="0a8f2-224">+$1</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-225">01191445550100 é convertido em +91445550100</span><span class="sxs-lookup"><span data-stu-id="0a8f2-225">01191445550100 is translated to +91445550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8f2-226">RedmondOperator</span><span class="sxs-lookup"><span data-stu-id="0a8f2-226">RedmondOperator</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-227">Converte 0 no operador de Redmond</span><span class="sxs-lookup"><span data-stu-id="0a8f2-227">Translates 0 to Redmond Operator</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-228">^0$</span><span class="sxs-lookup"><span data-stu-id="0a8f2-228">^0$</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-229">+14255550100</span><span class="sxs-lookup"><span data-stu-id="0a8f2-229">+14255550100</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-230">0 é convertido em +14255550100</span><span class="sxs-lookup"><span data-stu-id="0a8f2-230">0 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8f2-231">RedmondSitePrefix</span><span class="sxs-lookup"><span data-stu-id="0a8f2-231">RedmondSitePrefix</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-232">Converte números com o prefixo dentro da rede (6) e o código de área de Redmond (222)</span><span class="sxs-lookup"><span data-stu-id="0a8f2-232">Translates numbers with on-net prefix (6) and Redmond site code (222)</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-233">^ 6222 (\d {4} ) $</span><span class="sxs-lookup"><span data-stu-id="0a8f2-233">^6222(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-234">+1425555$1</span><span class="sxs-lookup"><span data-stu-id="0a8f2-234">+1425555$1</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-235">62220100 é convertido em +14255550100</span><span class="sxs-lookup"><span data-stu-id="0a8f2-235">62220100 is translated to +14255550100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8f2-236">NYSitePrefix</span><span class="sxs-lookup"><span data-stu-id="0a8f2-236">NYSitePrefix</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-237">Converte números com o prefixo dentro da rede (6) e o código de área de Nova York (333)</span><span class="sxs-lookup"><span data-stu-id="0a8f2-237">Translates numbers with on-net prefix (6) and NY site code (333)</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-238">^ 6333 (\d {4} ) $</span><span class="sxs-lookup"><span data-stu-id="0a8f2-238">^6333(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-239">+1202555$1</span><span class="sxs-lookup"><span data-stu-id="0a8f2-239">+1202555$1</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-240">63330100 é convertido em +12025550100</span><span class="sxs-lookup"><span data-stu-id="0a8f2-240">63330100 is translated to +12025550100</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8f2-241">DallasSitePrefix</span><span class="sxs-lookup"><span data-stu-id="0a8f2-241">DallasSitePrefix</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-242">Converte números com o prefixo dentro da rede (6) e o código de área de Dallas (444)</span><span class="sxs-lookup"><span data-stu-id="0a8f2-242">Translates numbers with on-net prefix (6) and Dallas site code (444)</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-243">^ 6444 (\d {4} ) $</span><span class="sxs-lookup"><span data-stu-id="0a8f2-243">^6444(\d{4})$</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-244">+1972555$1</span><span class="sxs-lookup"><span data-stu-id="0a8f2-244">+1972555$1</span></span></p></td>
<td><p><span data-ttu-id="0a8f2-245">64440100 é convertido em +19725550100</span><span class="sxs-lookup"><span data-stu-id="0a8f2-245">64440100 is translated to +19725550100</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0a8f2-246">A tabela a seguir ilustra um exemplo de plano de discagem para Redmond, Washington, Estados Unidos, com base nas regras de normalização mostradas na tabela anterior.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-246">The following table illustrates a sample dial plan for Redmond, Washington, United States, based on the normalization rules shown in the previous table.</span></span>

### <a name="table-2-redmond-dial-plan-based-on-normalization-rules-shown-in-table-1"></a><span data-ttu-id="0a8f2-p117">Tabela 2. Plano de discagem de Redmond com base em regras de normalização mostradas na Tabela 1</span><span class="sxs-lookup"><span data-stu-id="0a8f2-p117">Table 2. Redmond Dial Plan Based on Normalization Rules Shown in Table 1</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0a8f2-249">Redmond.forestFQDN</span><span class="sxs-lookup"><span data-stu-id="0a8f2-249">Redmond.forestFQDN</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a8f2-250">5digitExtension</span><span class="sxs-lookup"><span data-stu-id="0a8f2-250">5digitExtension</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8f2-251">7digitcallingRedmond</span><span class="sxs-lookup"><span data-stu-id="0a8f2-251">7digitcallingRedmond</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8f2-252">10digitcallingUS</span><span class="sxs-lookup"><span data-stu-id="0a8f2-252">10digitcallingUS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8f2-253">IntlCallingUS</span><span class="sxs-lookup"><span data-stu-id="0a8f2-253">IntlCallingUS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8f2-254">RedmondSitePrefix</span><span class="sxs-lookup"><span data-stu-id="0a8f2-254">RedmondSitePrefix</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8f2-255">NYSitePrefix</span><span class="sxs-lookup"><span data-stu-id="0a8f2-255">NYSitePrefix</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a8f2-256">DallasSitePrefix</span><span class="sxs-lookup"><span data-stu-id="0a8f2-256">DallasSitePrefix</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a8f2-257">RedmondOperator</span><span class="sxs-lookup"><span data-stu-id="0a8f2-257">RedmondOperator</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="0a8f2-p118">[!OBSERVAçãO] Os nomes das regras de normalização mostrados na tabela anterior não incluem espaços, mas é uma opção. O primeiro nome da tabela, por exemplo, poderia ter sido escrito "extensão de 5 dígitos" ou "Extensão de 5-dígitos" e ainda assim ser válido.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-p118">The normalization rules names shown in the preceding table do not include spaces, but this is a matter of choice. The first name in the table, for example, could have been written "5 digit extension" or "5-digit Extension" and still be valid.</span></span>



<span data-ttu-id="0a8f2-260"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0a8f2-260"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

