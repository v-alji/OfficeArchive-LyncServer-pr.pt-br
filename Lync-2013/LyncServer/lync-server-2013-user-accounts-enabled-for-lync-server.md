---
title: 'Lync Server 2013: contas de usuário habilitadas para o Lync Server'
description: 'Lync Server 2013: contas de usuário habilitadas para o Lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User accounts enabled for Lync Server 2013
ms:assetid: 8021087e-5084-4a39-9fef-ab9376c6d371
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182543(v=OCS.15)
ms:contentKeyID: 48184651
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf87177c378ffe61715d5332d2fd23b1d8e6fce6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "49390200"
---
# <a name="user-accounts-enabled-for-lync-server-2013"></a><span data-ttu-id="36270-103">Contas de usuário habilitadas para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36270-103">User accounts enabled for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36270-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36270-104">

<span> </span></span></span>

<span data-ttu-id="36270-105">_**Tópico da última modificação:** 2014-04-18_</span><span class="sxs-lookup"><span data-stu-id="36270-105">_**Topic Last Modified:** 2014-04-18_</span></span>

<span data-ttu-id="36270-106">Os tópicos desta seção fornecem procedimentos passo a passo para configurar as configurações do usuário que você pode executar usando o painel de controle do Lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="36270-106">Topics in this section provide step-by-step procedures for configuring user settings that you can perform using the Lync Server 2013 Control Panel.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="36270-107">Você não pode usar o painel de controle do Lync Server para gerenciar os usuários que são membros do grupo Administradores de domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="36270-107">You cannot use Lync Server Control Panel to manage users who are members of the Active Directory Domain Admins group.</span></span> <span data-ttu-id="36270-108">Para usuários de administradores de domínio, você pode usar o painel de controle do Lync Server somente para realizar operações de pesquisa somente leitura.</span><span class="sxs-lookup"><span data-stu-id="36270-108">For Domain Admins users, you can use Lync Server Control Panel only to perform read-only search operations.</span></span> <span data-ttu-id="36270-109">Para realizar operações de gravação em usuários de administradores de domínio (por exemplo, habilitar ou desabilitar o painel de controle do Lync Server, alterar as atribuições de grupo ou política, configurações de telefonia, endereço SIP), você deve usar cmdlets do Windows PowerShell enquanto estiver conectado como um usuário administradores de domínio.</span><span class="sxs-lookup"><span data-stu-id="36270-109">To perform write operations on Domain Admins users (for example, enable or disable for Lync Server Control Panel, change pool or policy assignments, telephony settings, SIP address), you must use Windows PowerShell cmdlets while logged on as a Domain Admins user.</span></span> <span data-ttu-id="36270-110">Para obter detalhes sobre como usar cmdlets do Windows PowerShell para gerenciar usuários, consulte <A href="lync-server-2013-lync-server-management-shell.md">Shell de gerenciamento do Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="36270-110">For details about using Windows PowerShell cmdlets to manage users, see <A href="lync-server-2013-lync-server-management-shell.md">Lync Server 2013 Management Shell</A>.</span></span>



</div>

<span data-ttu-id="36270-111">Quando você executa qualquer tarefa administrativa do Lync Server 2013 que envolve a pesquisa de um usuário ou filtragem dos resultados da pesquisa de usuário, existem algumas propriedades de usuário que existem como atributos nos serviços de domínio Active Directory, mas que não são replicadas para o catálogo global até que o Microsoft Exchange Server seja implantado.</span><span class="sxs-lookup"><span data-stu-id="36270-111">When you perform any Lync Server 2013 administrative task that involves searching for a user or filtering user search results, there are some user properties that exist as attributes in Active Directory Domain Services but are not replicated to the global catalog until Microsoft Exchange Server is deployed.</span></span> <span data-ttu-id="36270-112">Microsoft Exchange, não Lync Server, marca os seguintes atributos de replicação para o catálogo global quando ele é instalado:</span><span class="sxs-lookup"><span data-stu-id="36270-112">Microsoft Exchange, not Lync Server, marks the following attributes for replication to the global catalog when it is installed:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36270-113">Informações do usuário</span><span class="sxs-lookup"><span data-stu-id="36270-113">User Information</span></span></th>
<th><span data-ttu-id="36270-114">Endereço e telefone</span><span class="sxs-lookup"><span data-stu-id="36270-114">Address and Phone</span></span></th>
<th><span data-ttu-id="36270-115">Organização</span><span class="sxs-lookup"><span data-stu-id="36270-115">Organization</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36270-116">Iniciais</span><span class="sxs-lookup"><span data-stu-id="36270-116">Initials</span></span></p></td>
<td><p><span data-ttu-id="36270-117">Endereço da rua</span><span class="sxs-lookup"><span data-stu-id="36270-117">Street address</span></span></p>
<p><span data-ttu-id="36270-118">País/Região</span><span class="sxs-lookup"><span data-stu-id="36270-118">Country/region</span></span></p>
<p><span data-ttu-id="36270-119">Page</span><span class="sxs-lookup"><span data-stu-id="36270-119">Pager</span></span></p>
<p><span data-ttu-id="36270-120">Fax</span><span class="sxs-lookup"><span data-stu-id="36270-120">Fax</span></span></p>
<p><span data-ttu-id="36270-121">Mobile</span><span class="sxs-lookup"><span data-stu-id="36270-121">Mobile</span></span></p></td>
<td><p><span data-ttu-id="36270-122">Título</span><span class="sxs-lookup"><span data-stu-id="36270-122">Title</span></span></p>
<p><span data-ttu-id="36270-123">Empresa</span><span class="sxs-lookup"><span data-stu-id="36270-123">Company</span></span></p>
<p><span data-ttu-id="36270-124">Partamentais</span><span class="sxs-lookup"><span data-stu-id="36270-124">Department</span></span></p>
<p><span data-ttu-id="36270-125">Office</span><span class="sxs-lookup"><span data-stu-id="36270-125">Office</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="36270-126">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="36270-126">In This Section</span></span>

  - [<span data-ttu-id="36270-127">Exibir informações sobre contas de usuário habilitadas para o Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36270-127">Viewing information about user accounts enabled for Lync Server 2013</span></span>](lync-server-2013-viewing-information-about-user-accounts-enabled-for-lync-server.md)

  - [<span data-ttu-id="36270-128">Habilitando e desabilitando usuários do Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36270-128">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)

  - [<span data-ttu-id="36270-129">Gerenciando o Enterprise Voice para usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36270-129">Managing Enterprise Voice for users in Lync Server 2013</span></span>](lync-server-2013-managing-enterprise-voice-for-users.md)

  - [<span data-ttu-id="36270-130">Modificando Propriedades de conta de usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36270-130">Modifying user account properties in Lync Server 2013</span></span>](lync-server-2013-modifying-user-account-properties.md)

  - [<span data-ttu-id="36270-131">Gerenciar política de acesso externo no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36270-131">Manage external access policy in Lync Server 2013</span></span>](lync-server-2013-manage-external-access-policy-for-your-organization.md)

  - [<span data-ttu-id="36270-132">Como atribuir políticas por usuário no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36270-132">Assigning per-user policies in Lync Server 2013</span></span>](lync-server-2013-assigning-per-user-policies.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="36270-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="36270-133">See Also</span></span>


[<span data-ttu-id="36270-134">Cmdlets de gerenciamento de usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36270-134">User management cmdlets in Lync Server 2013</span></span>](lync-server-2013-user-management-cmdlets.md)  


[<span data-ttu-id="36270-135">Gerenciando usuários no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36270-135">Managing users in Lync Server 2013</span></span>](lync-server-2013-managing-users-in-lync-server.md)  
  

<span data-ttu-id="36270-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36270-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

