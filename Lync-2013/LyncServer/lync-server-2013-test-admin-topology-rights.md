---
title: 'Lync Server 2013: testar direitos de topologia de administração'
description: 'Lync Server 2013: testar direitos de topologia de administração.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test admin topology rights
ms:assetid: 0c03b7fd-449a-47ad-8263-ce811164cbce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767943(v=OCS.15)
ms:contentKeyID: 63969575
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22d713297d0e944c7acbc5efcb11b21ea1b26639
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441274"
---
# <a name="test-admin-topology-rights-in-lync-server-2013"></a><span data-ttu-id="6847f-103">Testar os direitos de topologia de administração no Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6847f-103">Test admin topology rights in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6847f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6847f-104">

<span> </span></span></span>

<span data-ttu-id="6847f-105">_**Tópico da última modificação:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="6847f-105">_**Topic Last Modified:** 2016-12-08_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6847f-106">Cronograma de verificação</span><span class="sxs-lookup"><span data-stu-id="6847f-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="6847f-107">Após a implantação inicial do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6847f-107">After initial Lync Server deployment.</span></span> <span data-ttu-id="6847f-108">Conforme necessário se surgirem problemas relacionados à permissão.</span><span class="sxs-lookup"><span data-stu-id="6847f-108">As needed if permission-related issues arise.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6847f-109">Ferramenta de teste</span><span class="sxs-lookup"><span data-stu-id="6847f-109">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="6847f-110">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6847f-110">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6847f-111">Permissões necessárias</span><span class="sxs-lookup"><span data-stu-id="6847f-111">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="6847f-112">Quando executado localmente usando o Shell de gerenciamento do Lync Server, os usuários devem ser membros do grupo de segurança RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="6847f-112">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="6847f-113">Quando executado usando uma instância remota do Windows PowerShell, os usuários devem receber uma função RBAC que tenha permissão para executar o cmdlet Test-CsSetupPermission.</span><span class="sxs-lookup"><span data-stu-id="6847f-113">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsSetupPermission cmdlet.</span></span> <span data-ttu-id="6847f-114">Para ver uma lista de todas as funções RBAC que podem usar esse cmdlet, execute o seguinte comando no prompt do Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="6847f-114">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsSetupPermission&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="6847f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="6847f-115">Description</span></span>

<span data-ttu-id="6847f-116">Por padrão, somente os administradores de domínio podem habilitar uma topologia do Lync Server e fazer grandes alterações na infraestrutura do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6847f-116">By default, only domain administrators can enable a Lync Server topology and make large changes to the Lync Server infrastructure.</span></span> <span data-ttu-id="6847f-117">Isso não será um problema, contanto que seus administradores de domínio e seus administradores do Lync Server sejam os mesmos. Em muitas organizações, os administradores do Lync Server não mantêm direitos administrativos para todo o domínio.</span><span class="sxs-lookup"><span data-stu-id="6847f-117">This won't be a problem as long as your domain administrators and your Lync Server administrators are one and the same.In many organizations Lync Server administrators do not hold administrative rights to the whole domain.</span></span> <span data-ttu-id="6847f-118">Por padrão, isso significa que esses administradores (definidos como membros do grupo RTCUniversalServerAdmins) não podem fazer alterações de topologia do Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6847f-118">By default, that means that these administrators (defined as members of the RTCUniversalServerAdmins group) can't make Lync Server topology changes.</span></span> <span data-ttu-id="6847f-119">Para dar aos membros do grupo RTCUniversalServerAdmins o direito de fazer alterações de topologia, você deve atribuir as permissões necessárias do Active Directory usando o cmdlet [Grant-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission) .</span><span class="sxs-lookup"><span data-stu-id="6847f-119">To give members of the RTCUniversalServerAdmins group the right to make topology changes, you must assign the required Active Directory permissions by using the [Grant-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission) cmdlet.</span></span>

<span data-ttu-id="6847f-120">O cmdlet Test-CsSetupPermission verifica se as permissões necessárias para instalar o Lync Server ou um de seus componentes estão configuradas no contêiner especificado do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6847f-120">The Test-CsSetupPermission cmdlet verifies that the required permissions that are needed to install Lync Server or one of its components are configured on the specified Active Directory container.</span></span> <span data-ttu-id="6847f-121">Se as permissões não forem atribuídas, você poderá executar o cmdlet Grant-CsSetupPermission para dar aos membros do grupo RTCUniversalServerAdmins o direito de instalar e habilitar o Lync Server.</span><span class="sxs-lookup"><span data-stu-id="6847f-121">If the permissions are not assigned, you can then run the Grant-CsSetupPermission cmdlet to give members of the RTCUniversalServerAdmins group the right to install and enable Lync Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6847f-122">Para obter uma lista detalhada de permissões atribuídas por Grant-CsSetupPermission, consulte a <A href="https://blogs.technet.com/b/jenstr/archive/2011/02/07/grant-cssetuppermission-and-grant-csoupermission.aspx">concessão do blog-CsSetupPermission e Grant-CsOUPermission</A>.</span><span class="sxs-lookup"><span data-stu-id="6847f-122">For a detailed list of permissions assigned by Grant-CsSetupPermission, see the blog post <A href="https://blogs.technet.com/b/jenstr/archive/2011/02/07/grant-cssetuppermission-and-grant-csoupermission.aspx">Grant-CsSetupPermission and Grant-CsOUPermission</A>.</span></span>



</div>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="6847f-123">Executar o teste</span><span class="sxs-lookup"><span data-stu-id="6847f-123">Running the test</span></span>

<span data-ttu-id="6847f-124">Para determinar se as permissões de configuração foram atribuídas para um contêiner do Active Directory, chame o cmdlet Test-CsSetupPermission.</span><span class="sxs-lookup"><span data-stu-id="6847f-124">To determine whether setup permissions are assigned for an Active Directory container, call the Test-CsSetupPermission cmdlet.</span></span> <span data-ttu-id="6847f-125">Especifique o nome diferenciado do contêiner a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="6847f-125">Specify the distinguished name of the container to be checked.</span></span> <span data-ttu-id="6847f-126">Por exemplo, esse comando verifica as permissões de configuração no container ou = CsServers, DC = litwareinc, DC = com:</span><span class="sxs-lookup"><span data-stu-id="6847f-126">For example, this command verifies setup permissions on the container ou=CsServers,dc=litwareinc,dc=com:</span></span>

    Test-CsSetupPermission -ComputerOU "ou=CsServers,dc=litwareinc,dc=com"

<span data-ttu-id="6847f-127">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) .</span><span class="sxs-lookup"><span data-stu-id="6847f-127">For more information, see the help topic for the [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="6847f-128">Determinação do sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="6847f-128">Determining success or failure</span></span>

<span data-ttu-id="6847f-129">Se Test-CsSetupPermission determinar que as permissões necessárias já foram definidas em um contêiner do Active Directory, o cmdlet retornará o valor true:</span><span class="sxs-lookup"><span data-stu-id="6847f-129">If Test-CsSetupPermission determines that the required permissions have already been set on an Active Directory container then the cmdlet will return the value True:</span></span>

<span data-ttu-id="6847f-130">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="6847f-130">True</span></span>

<span data-ttu-id="6847f-131">Se as permissões não estiverem definidas, Test-CsSetupPermission retornará o valor false.</span><span class="sxs-lookup"><span data-stu-id="6847f-131">If permissions are not set, Test-CsSetupPermission will return the value False.</span></span> <span data-ttu-id="6847f-132">Observe que esse valor normalmente será incluído em muitas mensagens de aviso.</span><span class="sxs-lookup"><span data-stu-id="6847f-132">Note that this value will typically be enclosed in many warning messages.</span></span> <span data-ttu-id="6847f-133">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6847f-133">For example:</span></span>

<span data-ttu-id="6847f-134">Aviso: entrada de controle de acesso (ACE) ATL-cs-001 \\ RTCUniversalServerAdmins; Habilitar ExtendedRight; Nenhuma Nenhuma 1131f6aa-9c07-11d1-f79f-00c04fc2dcd2</span><span class="sxs-lookup"><span data-stu-id="6847f-134">WARNING: Access control entry (ACE) atl-cs-001\\RTCUniversalServerAdmins; Allow; ExtendedRight; None; None; 1131f6aa-9c07-11d1-f79f-00c04fc2dcd2</span></span>

<span data-ttu-id="6847f-135">Aviso: as entradas de controle de acesso (ACEs) no objeto "CN = Computers, DC = litwareinc, DC = com" não estão prontas.</span><span class="sxs-lookup"><span data-stu-id="6847f-135">WARNING: The access control entries (ACEs) on the object "CN=Computers,DC=litwareinc,DC=com" are not ready.</span></span>

<span data-ttu-id="6847f-136">Falso</span><span class="sxs-lookup"><span data-stu-id="6847f-136">False</span></span>

<span data-ttu-id="6847f-137">Aviso: o processamento de "Test-CsSetupPermission" foi concluído com avisos.</span><span class="sxs-lookup"><span data-stu-id="6847f-137">WARNING: "Test-CsSetupPermission" processing has completed with warnings.</span></span> <span data-ttu-id="6847f-138">"2" avisos foram registrados durante a execução.</span><span class="sxs-lookup"><span data-stu-id="6847f-138">"2" warnings were recorded during this run.</span></span>

<span data-ttu-id="6847f-139">Aviso: os resultados detalhados podem ser encontrados em "C: \\ Users \\ admin \\ AppData \\ local \\ temp \\Test-CsSetupPermission-1da99ba6-abe2-45e4-8b16-dfd244763118.html".</span><span class="sxs-lookup"><span data-stu-id="6847f-139">WARNING: Detailed results can be found at "C:\\Users\\Admin\\AppData\\Local\\Temp\\Test-CsSetupPermission-1da99ba6-abe2-45e4-8b16-dfd244763118.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="6847f-140">Motivos pelos quais o teste pode ter falhado</span><span class="sxs-lookup"><span data-stu-id="6847f-140">Reasons why the test might have failed</span></span>

<span data-ttu-id="6847f-141">Embora existam exceções raras, se Test-CsSetupPermission falhar, geralmente significa que as permissões de configuração não são atribuídas ao contêiner do Active Directory especificado.</span><span class="sxs-lookup"><span data-stu-id="6847f-141">Although there are rare exceptions, if Test-CsSetupPermission fails that typically means that setup permissions are not assigned for the specified Active Directory container.</span></span> <span data-ttu-id="6847f-142">Essas permissões podem ser atribuídas usando o cmdlet Grant-CsSetupPermission.</span><span class="sxs-lookup"><span data-stu-id="6847f-142">Those permissions can be assigned by using the Grant-CsSetupPermission cmdlet.</span></span> <span data-ttu-id="6847f-143">Por exemplo, esse comando concede permissões de configuração para o contêiner de computadores no domínio litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="6847f-143">For example, this command grants setup permissions to the Computers container in the domain litwareinc.com:</span></span>

    Grant-CsSetupPermission -ComputerOU "cn=Computers,dc=litwareinc,dc=com"

<span data-ttu-id="6847f-144">Para obter mais informações, consulte o tópico da ajuda para o cmdlet [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) .</span><span class="sxs-lookup"><span data-stu-id="6847f-144">For more information, see the help topic for the [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) cmdlet.</span></span>

<span data-ttu-id="6847f-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6847f-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

